# Entity Relationship Diagram

- The ER diagram has three main tables: **User**, **Expense**, and **Category**.  
- Each **User** can have multiple **Expenses**, and each **Expense** belongs to a single **Category**.  
- The relationships ensure that all data is linked correctly, allowing the system to track user expenses by category efficiently.


```mermaid

erDiagram

    USERS {
        INT id PK
        VARCHAR username
        VARCHAR email
        VARCHAR password
        TIMESTAMP created_at
        TIMESTAMP updated_at
        TIMESTAMP deleted_at
    }

    CATEGORIES {
        INT id PK
        VARCHAR name
    }

    TRANSACTIONS {
        INT id PK
        INT user_id FK
        INT category_id FK
        BOOLEAN is_income
        NUMERIC amount
        TEXT description
        DATE date_of_transaction
        TIMESTAMP created_at
        TIMESTAMP updated_at
        TIMESTAMP deleted_at
    }

    USERS ||--o{ TRANSACTIONS : "has many"
    CATEGORIES ||--o{ TRANSACTIONS : "has many"

```


**Next:** [Data Flow Diagram ->](Data-Flow.md)