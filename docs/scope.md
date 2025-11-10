# Scope

## In-Scope

### 1. User Authentication

*   Secure **login and registration** using encrypted credentials.
    
*   Passwords stored securely using encryption mechanisms.
    
*   Access control to ensure only authenticated users can view their data.
    

### 2. Transaction Management

*   Complete **CRUD operations** (Create, Read, Update, Delete) for expense and income records.
    
*   Each transaction includes amount, category, description, and date fields.
    

### 3. Categorization of Expenses

*   Users can assign each transaction to a specific category such as **Food, Transport, Bills, Savings**, etc.
    
*   Enables better financial analysis and spending insights.
    

### 4. Overview Dashboard

The first page after login displays key financial insights including:

*   **Monthly Income Section** – Displays total income for the current month.
    
*   **Monthly Expense Chart (Pie Chart)** – Visual breakdown of monthly spending in the form of pie chart.
    
*   **Last Month’s Summary** – Highlights previous month’s expenses and income in the form of pie chart.
    
*   **Recent Transactions Section** – Displays the latest income and expense entries.
    

### 5. Sidebar Navigation

A persistent left-side menu providing quick access to main modules:

*  **Overview** – Summary dashboard.
    
*  **Transactions** – Detailed transaction list and management.
    
*  **Import/Export** – Generate and download PDF reports of monthly transactions.
    

### 6. Transactions Page

*   Dedicated page to view, add, and manage transactions.
    
*   **Add Income (➕)** and **Add Expense (➖)** buttons for quick entry.
    
*   **Filter Functionality** to view older or category-specific transactions.
    

### 7. Report Generation

*   Users can **export monthly financial summaries** as PDF reports.
    
*   Reports include categorized breakdowns, totals, and summary visuals.
    

### 8. Logout Functionality

*   Secure **sign-out option** available in the top-right corner.
    
*   Ensures safe session termination and data protection.
    

### 9. Cross-Device Accessibility (PWA)

*   Application is fully **responsive and mobile-accessible** through Progressive Web App (PWA) design.
    
*   Allows users to install and access the app like a native mobile application


## Out of Scope / Future Enhancements

The following features are **not included** in the initial version of the *Personal Expense Tracker* but are planned for **future development** to enhance functionality, usability, and scalability:

### 1. Budget Goal Setting & Alerts

   Allow users to define monthly or category-specific budgets and receive notifications when approaching or exceeding spending limits.  
   This feature will help users manage their finances more effectively by setting personal spending goals and tracking progress visually.

### 2. Advanced Analytics & AI-Driven Insights 

   Incorporate data analytics and machine learning to identify spending trends, forecast future expenses, and provide personalized financial insights.  
   This enhancement will enable intelligent decision-making and help users gain deeper understanding of their spending habits.

### 3. Screenshot Upload & Cloud Storage (AWS S3 Integration)

   Allow users to upload a screenshot or image of the transaction receipt **while creating a transaction**, which will be securely stored in an AWS S3 bucket.  
   This feature improves record-keeping, enhances verification, and ensures that transaction details are backed up securely in the cloud and provides ease for the customer.


**Next:** [Requirements ->](Requirements.md)