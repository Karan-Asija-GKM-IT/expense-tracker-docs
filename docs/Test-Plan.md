# Personal Expense Tracker - Test Plan

## 1. Objective & Scope

### Objective:  
To ensure the Personal Expense Tracker app functions correctly, securely, and efficiently for end-users in tracking income and expenses. The focus is on functional correctness, usability, data integrity, and security.

### Scope:  
- Functional testing of user registration, login, and authentication.  
- CRUD operations for expenses (add, edit, delete).  
- Viewing expense summaries and reports.  
- Input validation.  
- API functionality and database integration with PostgreSQL.  

### Out of Scope:
The following non-functional aspects are not in the scope of testing: **performance, usability, portability, reliability, and compatibility.**  
Since the app is intended for English-speaking users, no language testing (internationalization) is planned.  

---

## 2. Test Strategy

- **Testing Types:** Functional testing and unit testing.  
- **Approach:**  
  - Unit tests for backend logic using **Jest**.  
  - API tests using **Postman**.  
  - Manual testing for UI/UX and workflow verification.  

---

## 3. Test Coverage Goals

- Ensure all core features (registration, login, CRUD operations, reports) work as expected.  
- Validate correct input handling and error messages.  
- Verify data consistency between frontend, backend, and database.  
- Ensure authentication and authorization mechanisms are secure.  
- Detect UI/UX issues affecting user interaction.  

---

## 4. Execution Plan

- **Test Preparation:**  
  - Set up test environment.  
  - Create and configure test data.  

- **Test Execution:**  
  - Execute unit tests on backend endpoints.  
  - Perform manual testing of frontend workflows. 
  - Validate API responses using Postman.
  - Retest after bug fixes.  

---

## 5. Entry & Exit Criteria

**Entry Criteria:**  
- Backend and frontend deployed in test environment.
- Test data prepared.  
- Test environment stable and accessible.  

**Exit Criteria:**  
- All planned test cases executed.  
- Critical and high-severity defects resolved.  

---

## 6. Risks & Mitigation

| Risk | Mitigation |
|------|-------------|
| Incorrect expense calculations | Write unit tests to check all calculations. |
| Errors in user login or registration | Test authentication and input validation thoroughly. |
| Data issues in the database | Use mock data and verify all CRUD operations work correctly. |
| Bugs in backend code | Write unit tests for all functions and fix any failing tests. |
| Missing test coverage | Check Jest coverage reports and add tests for untested code. |


**Next:** [Deployment Flow ->](Deployment.md)