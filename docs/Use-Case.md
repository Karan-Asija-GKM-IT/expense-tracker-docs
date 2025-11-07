**Use Case Descriptions**

**Use Case 1 — Register Account**

**Actor:** User

**Pre-condition:** No existing account.

**Main Flow:**

1.  User clicks “Register”.
    
2.  Inputs email & password.
    
3.  System validates and stores credentials.
    
**Post-condition:** Account created; redirect to login page.

**Use Case 2 — Login**

**Actor:** User

**Pre-condition:** Valid credentials exist.

**Main Flow:**

1.  User enters email and password.
    
2.  System authenticates.
    
3.  Redirect to Dashboard.
    
**Post-condition:** User session started.

**Use Case 3 — View Dashboard**

**Actor:** User

**Pre-condition:** Logged in.

**Main Flow:**

1.  System loads Overview Dashboard.
    
2.  Displays income, weekly expenses (pie chart), last month summary, and recent transactions.
    

**Post-condition:** User views financial snapshot.

**Use Case 4 — Add Income/Expense**

**Actor:** User

**Pre-condition:** Logged in.

**Main Flow:**

1.  Navigate to Transactions page.
    
2.  Click ➕ (Add Income) or ➖ (Add Expense).
    
3.  Enter details (amount, category, date, description).
    
4.  Click “Save”.

**Post-condition:** Transaction recorded and dashboard updated.

**Use Case 5 — Edit or Delete Transaction**

**Actor:** User

**Pre-condition:** Transaction exists.

**Main Flow:**

1.  Select transaction.
    
2.  Edit details → Save OR Click Delete → Confirm.
    
3.  System updates or removes record.
    
**Post-condition:** Data updated in database and UI.

**Use Case 6 — Filter Transactions**

**Actor:** User

**Pre-condition:** Transaction list available.

**Main Flow:**

1.  Apply filter (date range or month).
    
2.  System returns filtered records.
    
**Post-condition:** Filtered list displayed.

**Use Case 7 — Generate Monthly Report**

**Actor:** User

**Pre-condition:** At least one month’s transactions.

**Main Flow:**

1.  Navigate to Import/Export.
    
2.  Select month.
    
3.  System fetches and aggregates data.
    
4.  PDF report generated for download.
    
**Post-condition:** Report saved locally / viewed on-screen.

**Use Case 8 — Logout**

**Actor:** User

**Main Flow:**

1.  Click “Sign Out”.
    
2\. System terminates session and redirects to login.

**Post-condition:** User logged out securely.