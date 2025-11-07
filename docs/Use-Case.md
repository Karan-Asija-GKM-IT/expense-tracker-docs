# Technical Use Cases

Below are the detailed technical use cases for the **Personal Expense Tracker** application.

---

## 1. Register Account

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | No existing account. |
| **Main Flow** | 1. User clicks “Register”.<br>2. Inputs email & password.<br>3. System validates and stores credentials. |
| **Post-condition** | Account created; redirect to login page. |

---

## 2. Login

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | Valid credentials exist. |
| **Main Flow** | 1. User enters email and password.<br>2. System authenticates.<br>3. Redirect to Dashboard. |
| **Post-condition** | User session started. |

---

## 3. View Dashboard

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | Logged in. |
| **Main Flow** | 1. System loads Overview Dashboard.<br>2. Displays income, weekly expenses (pie chart), last month summary, and recent transactions. |
| **Post-condition** | User views financial snapshot. |

---

## 4. Add Income/Expense

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | Logged in. |
| **Main Flow** | 1. Navigate to Transactions page.<br>2. Click ➕ (Add Income) or ➖ (Add Expense).<br>3. Enter details (amount, category, date, description).<br>4. Click “Save”. |
| **Post-condition** | Transaction recorded and dashboard updated. |

---

## 5. Edit or Delete Transaction

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | Transaction exists. |
| **Main Flow** | 1. Select transaction.<br>2. Edit details → Save OR Click Delete → Confirm.<br>3. System updates or removes record. |
| **Post-condition** | Data updated in database and UI. |

---

## 6. Filter Transactions

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | Transaction list available. |
| **Main Flow** | 1. Apply filter (date range or month).<br>2. System returns filtered records. |
| **Post-condition** | Filtered list displayed. |

---

## 7. Generate Monthly Report

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | At least one month’s transactions. |
| **Main Flow** | 1. Navigate to Import/Export.<br>2. Select month.<br>3. System fetches and aggregates data.<br>4. PDF report generated for download. |
| **Post-condition** | Report saved locally or viewed on-screen. |

---

## 8. Logout

| **Attribute** | **Description** |
|----------------|-----------------|
| **Actor** | User |
| **Pre-condition** | Active session. |
| **Main Flow** | 1. Click “Sign Out”.<br>2. System terminates session and redirects to login. |
| **Post-condition** | User logged out securely. |

---

**Next:** [System Architecture →](architecture.md)
