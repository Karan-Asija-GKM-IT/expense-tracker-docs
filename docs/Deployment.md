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

---

### **a. Backend Unit Tests (Jest)**  
Job: `backend-tests`

- Installs dependencies  
- Runs Jest test cases  
- Generates code coverage  
- Uploads coverage report to GitHub Actions Artifacts  

This ensures new changes do not break existing backend logic.

---

### **b. Security Scanning (SAST with Trivy)**  
Job: `trivy-sast`

- Scans the full codebase for:
  - Secrets  
  - Misconfigurations  
  - High/Critical vulnerabilities  
- Fails the pipeline if severe issues are detected

This ensures the code pushed into the branch is secure.

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

