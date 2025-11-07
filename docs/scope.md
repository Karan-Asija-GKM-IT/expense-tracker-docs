

### **1.1. In-Scope**

#### **i. User Authentication**

*   Secure **login and registration** using encrypted credentials.
    
*   Passwords stored securely using encryption mechanisms.
    
*   Access control to ensure only authenticated users can view their data.
    

#### **ii. Transaction Management**

*   Complete **CRUD operations** (Create, Read, Update, Delete) for expense and income records.
    
*   Each transaction includes amount, category, description, and date fields.
    

#### **iii. Categorization of Expenses**

*   Users can assign each transaction to a specific category such as **Food, Transport, Bills, Savings**, etc.
    
*   Enables better financial analysis and spending insights.
    

#### **iv. Overview Dashboard**

The first page after login displays key financial insights including:

*   **Monthly Income Section** – Displays total income for the current month.
    
*   **Weekly Expense Chart (Pie Chart)** – Visual breakdown of weekly spending by category.
    
*   **Last Month’s Summary** – Highlights previous month’s total expenses and savings comparison.
    
*   **Recent Transactions Section** – Displays the latest income and expense entries.
    

#### **v. Sidebar Navigation**

A persistent left-side menu providing quick access to main modules:

1.  **Overview** – Summary dashboard.
    
2.  **Transactions** – Detailed transaction list and management.
    
3.  **Import/Export** – Generate and download PDF reports of monthly transactions.
    

#### **vi. Transactions Page**

*   Dedicated page to view, add, and manage transactions.
    
*   **Add Income (➕)** and **Add Expense (➖)** buttons for quick entry.
    
*   **Filter Functionality** to view older or category-specific transactions.
    

#### **vii. Report Generation**

*   Users can **export monthly financial summaries** as PDF reports.
    
*   Reports include categorized breakdowns, totals, and summary visuals.
    

#### **viii. Logout Functionality**

*   Secure **sign-out option** available in the top-right corner.
    
*   Ensures safe session termination and data protection.
    

#### **ix. Cross-Device Accessibility (PWA)**

*   Application is fully **responsive and mobile-accessible** through Progressive Web App (PWA) design.
    
*   Allows users to install and access the app like a native mobile application


### **1.2\. Out of Scope / Future Enhancements**

The following features are currently **out of scope** for the initial version of the Personal Expense Tracker but are planned for future development to enhance functionality and user experience:

1.  **Budget Goal Setting & Alerts**
    
    *   Allow users to define monthly or category-specific budgets and receive alerts when nearing or exceeding limits.
        
2.  **Multi-Language Interface & Localization**
    
    *   Provide support for multiple languages and regional settings to make the app accessible globally.
        
3.  **Advanced Analytics & AI-Driven Insights**
    
    *   Implement machine learning models to analyze spending behavior, predict future expenses, and offer personalized financial advice.
        
4.  **Bank Account Integration**
    
    *   Enable automatic import of transactions from linked bank accounts through secure API integration.
        
5.  **Push Notifications & Offline Data Sync**
    
    *   Allow users to receive timely updates, reminders, and access app data offline with automatic sync once reconnected.
        
6.  **Multi-User or Shared Accounts**
    
    *   Introduce shared or family expense tracking with role-based permissions and collaborative dashboards.


**Next:** [Requirements ->](Requirements.md)