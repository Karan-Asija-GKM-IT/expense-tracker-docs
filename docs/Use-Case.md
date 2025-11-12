# Business Use Cases

Below are the key business use cases for the **Personal Expense Tracker** application.  

---

## 1. Manage Personal Finances

| **Attribute** | **Description** |
|----------------|-----------------|
| **Business Objective** | Enable users to track and manage their income and expenses efficiently. |
| **Actor** | User |
| **Pre-condition** | User has registered and logged in successfully. |
| **Main Flow** | 1. User records income and expenses under some category.<br>2. System stores the transactions.<br>3. User views summary through the dashboard. |
| **Post-condition** | User gains visibility into spending and overall financial health. |
| **Business Value** | Increases financial discipline and decision-making through organized record-keeping. |

---

## 2. Analyze Spending Patterns

| **Attribute** | **Description** |
|----------------|-----------------|
| **Business Objective** | Provide users with insights into their spending habits. |
| **Actor** | User |
| **Pre-condition** | Transaction data exists in the system. |
| **Main Flow** | 1. System aggregates data by category and date.<br>2. Generates pie charts for monthly expense.<br>3. Displays insights on dashboard. |
| **Post-condition** | User identifies major expense areas and adjusts habits. |
| **Business Value** | Encourages smarter budgeting and financial awareness. |

---

## 3. Generate Monthly Financial Reports

| **Attribute** | **Description** |
|----------------|-----------------|
| **Business Objective** | Allow users to generate and export monthly expense reports for personal or professional use. |
| **Actor** | User |
| **Pre-condition** | Minimum one month of data is recorded. |
| **Main Flow** | 1. User selects the month for which report is needed.<br>2. System compiles transactions into a .csv file.<br>3. Report is made available for download. |
| **Post-condition** | .CSV downloaded. |
| **Business Value** | Provides documentation for budgeting purposes.|

---

# Technical Use Cases

Below are the detailed technical use cases for the **Personal Expense Tracker** application.

---

## 1. Login / Register

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | User must have valid credentials or register a new account. |
| **Main Flow** | 1. User selects *Login* or *Register* option.<br>2. Provides required details (email, password, etc.).<br>3. System validates credentials or creates a new user account.<br>4. On success, user is redirected to the dashboard. |
| **Post-condition** | User gains access to their personal expense dashboard. |

---

## 2. View Dashboard

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | User must be logged in. |
| **Main Flow** | 1. System fetches and displays user’s income, expense summaries, recent transactions, and comparison charts.<br>2. User can navigate to other modules via side menu. |
| **Post-condition** | Dashboard data successfully displayed. |

---

## 3. Manage Transactions

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | User is logged in and has access to transaction module. |
| **Main Flow** | 1. User navigates to *Transactions* page.<br>2. User can add new transactions (income/expense) with details such as category, amount, description, and date.<br>3. User can filter, edit, or delete existing transactions. |
| **Post-condition** | Transaction data is updated in the database and reflected on the dashboard. |

---

## 4. Generate Monthly Report

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | At least one transaction exists for the selected month. |
| **Main Flow** | 1. User selects a month or date range.<br>2. System calculates total income, total expense, and savings.<br>3. System generates a summary report, downloadable as a .csv file. |
| **Post-condition** | Monthly report generated and displayed to the user. |

---

## 5. Logout

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | User is logged in. |
| **Main Flow** | 1. User clicks on *Logout* button.<br>2. System invalidates user session and redirects to the login screen. |
| **Post-condition** | User is securely logged out of the system. |

---

# Use Case Diagram


![Expense Tracker App Use Case Diagram](Use-Case-Diagram copy.png)

**Next:** [Data Modeling ->](Data-Modeling.md)