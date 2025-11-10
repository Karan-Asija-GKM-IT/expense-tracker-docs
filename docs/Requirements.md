# Functional Requirements


# Functional Requirements

| **Category** | **Description** |
|:---------------------------|:--------------------------------------------------------------------------------|
| **User Registration & Login** | Secure signup/login using email and password. |
| **Dashboard Overview** | Display monthly income, weekly expense pie chart, last month summary, and transactions. |
| **Sidebar Navigation** | Navigate between Overview, Transactions, and Import/Export. |
| **Add Transaction** | Add a new transaction by entering amount, description, date, and selecting type (Income or Expense). The category list updates dynamically based on the selected type. |
| **Edit/Delete Transactions** | Modify or remove an existing record. |
| **Transaction Filters** | Filter transactions by date range or category. |
| **Report Generation (PDF)** | Export monthly transactions as a downloadable PDF. |
| **Logout Functionality** | Securely end session and redirect to login page. |



# Non-functional Requirements

| **Category**         | **Description**                                                                                             |
|:-----------------|:------------------------------------------------------------------------------------------------------------|
| Performance      | The system should load and display data within 3 seconds for standard use.                                  |
| Usability        | The UI shall be responsive and accessible across devices (desktop, tablet, mobile).                         |
| Security         | Passwords shall be stored in encrypted format. User data shall be protected from unauthorized access.        |
| Reliability      | The system shall ensure data persistence and integrity after user sessions.                                 |
| Maintainability  | Code shall follow modular architecture with separation of concerns (frontend, backend, database).            |
| Scalability      | The system should be designed to support future enhancements such as budget tracking or analytics.           |



**Next:** [Use Cases ->](Use-Case.md)