# Scans & Test Coverage 

## SAST Scan 

**SAST** refers to scanning the application's source code, configuration files, and dependencies **without executing the application**.  
Its purpose is to identify security issues early in the development lifecycle.

#### Tool Used: Trivy

Trivy is an open-source security scanner developed by Aqua Security.  
It is used to detect:

- Vulnerable or outdated packages  
- Hard-coded secrets  
- Misconfigurations in code or infrastructure files  
- Critical or High-severity issues in the codebase  

Trivy was chosen because it is:

- Fast and lightweight.
- Easy to integrate with GitHub Actions.
- Provides accurate vulnerability reports.

![SAST Scan](Trivy-Scan-SAST.png)

---

## DAST Scan 

**DAST** scans the application *after it is deployed* to identify runtime security weaknesses.  
It analyzes the live API by sending automated attack patterns and detecting vulnerabilities such as:

- Authentication weaknesses  
- Cross-Site Scripting (XSS)  
- SQL Injection  
- Broken access control  
- Missing or insecure security headers  

#### Tool Used: OWASP ZAP

**OWASP ZAP (Zed Attack Proxy)** is the DAST tool used in this project. It is:

- One of the most widely used open-source penetration testing tools.  
- Actively maintained by the OWASP foundation.
- Capable of scanning real HTTP endpoints.  
- Able to generate detailed vulnerability and risk reports.  

OWASP ZAP is ideal for API security scanning because it supports:

- GET and POST endpoints.  
- Authenticated and unauthenticated scans.  
- Passive and active scanning.  
- OWASP Top 10 vulnerability coverage.  

![DAST Scan](DAST-SCAN.png)

---

## Test Coverage Report

Test coverage is an important metric used to evaluate how much of the backend codebase is executed during automated testing.  
It helps ensure that critical business logic, services, utilities, and controllers are properly tested before deployment.

The project uses **Jest** to generate detailed coverage reports every time tests run—both locally and inside the CI/CD pipeline.

#### What the Coverage Report Includes

The Jest coverage report provides insights into:

- **Line Coverage** – Percentage of code lines executed  
- **Statement Coverage** – Percentage of executed statements  
- **Function Coverage** – How many functions were invoked  
- **Branch Coverage** – Coverage of `if`, `switch`, and logical branches  

This allows developers to identify untested code paths and improve overall quality.

![Test Coverage Report](Test-Coverage-Report.png)

---

## Github Actions Report 

![Github Actions Report](Actions-report.png)
