## Code Merge Workflow

This project uses a simplified and automated merge workflow designed around direct branch pushes.  
The CI/CD pipeline is triggered **whenever code is pushed to the `feat/tests` branch`.  
This ensures that all updates to this branch automatically go through testing, security scanning, and deployment.

### 1. Branching Strategy

The project follows a minimal branching model:

- **feat/tests** — The main development branch where CI/CD is triggered.
- **Other feature branches** (optional) may be created locally but must be pushed into `feat/tests` for deployment.

### 2. Code Update Flow

1. Developer writes code locally.
2. Commits the changes.
3. Pushes directly to the `feat/tests` branch.

Once the push is detected, GitHub Actions automatically begins the CI/CD pipeline.

### 3. Automated Pipeline Stages on Push

When code is pushed to the branch, the following jobs run **automatically**:

### **a. Backend Unit Tests (Jest)**  
Job: `backend-tests`

- Installs dependencies  
- Runs Jest test cases  
- Generates code coverage  
- Uploads coverage report to GitHub Actions Artifacts  

This ensures new changes do not break existing backend logic.
```
jobs:
  backend-tests:
    name: Run Backend Tests
    runs-on: ubuntu-latest
    
    steps:
      - name: Checkout Code
        uses: actions/checkout@v4

      - name: Setup Node
        uses: actions/setup-node@v4
        with:
          node-version: 24.9.0

      - name: Install Dependencies
        run: npm install

      - name: Run Jest Tests with Coverage
        run: npm run test -- --coverage

      - name: Upload Coverage Report
        uses: actions/upload-artifact@v4
        with:
          name: backend-coverage-report
          path: coverage
```
---

### **b. Security Scanning (SAST with Trivy)**  
Job: `trivy-sast`

- Scans the full codebase for:
  - Secrets  
  - Misconfigurations  
  - High/Critical vulnerabilities  
- Fails the pipeline if severe issues are detected

This ensures the code pushed into the branch is secure.

```
trivy-sast:
    name: Trivy SAST Scan
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4
      - name: Run Trivy SAST
        uses: aquasecurity/trivy-action@master
        with:
          scan-type: "fs"
          scanners: "secret,misconfig"
          scan-ref: "."
          exit-code: "1"
          severity: "CRITICAL,HIGH"
```
---

### **c. Deployment to AWS EC2**  
Job: `deploy`

If the previous jobs succeed, deployment begins automatically:

- Connects to EC2 using SSH  
- Pulls the latest code from the `feat/tests` branch  
- Installs production dependencies  
- Restarts the application using PM2  
- Confirms successful deployment  

This provides a fully automated deployment cycle.

```
deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4
      - name: Set up SSH
        uses: webfactory/ssh-agent@v0.9.0
        with:
          ssh-private-key: ${{ secrets.EC2_SSH_KEY }}
      - name: Deploy to EC2
        run: |
          ssh -o StrictHostKeyChecking=no ${{ secrets.EC2_USER }}@${{ secrets.EC2_HOST }} << 'EOF'
            echo "---- Pulling latest changes ----"
            cd /expense-tracker-backend
            git fetch --all
            git reset --hard origin/feat/tests
            echo "---- Installing dependencies ----"
            npm install --production
            echo "---- Restarting server ----"
            pm2 restart all
            echo "---- Deployment Completed Successfully ----"
```

### 4. Summary of the Merge Workflow

| Step | Action | Description |
|------|--------|-------------|
| 1 | Push to `feat/tests` | Developer pushes code to this branch |
| 2 | Backend Tests Run | Jest tests + Coverage |
| 3 | Security Scan | Trivy SAST check |
| 4 | Deployment | Automatic EC2 deployment via SSH |
| 5 | App Live | Updated backend live after PM2 restart |

### 5. Notes

- No Pull Requests (PRs) are used in this workflow.  
- Deployment only happens for the `feat/tests` branch.  
- The workflow ensures code quality through test execution and SAST scanning before deployment.

---

