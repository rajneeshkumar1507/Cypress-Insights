## Page Object Model (POM) in Cypress: Detailed Notes with Examples

### Overview
- **POM**
  - A design pattern that enhances the maintainability and readability of test automation scripts.
- **Purpose**
  - Separates test logic from page-specific code, making tests cleaner and easier to manage.

---

### Key Concept

**1. Page Objects:**
- **Definition:**
  - Classes or modules that represent individual pages or components of your application.
- **Example:**
  - For a login page, create a `LoginPage` object to manage all interactions with that page.

<br>

**2. Separation of Concerns:**
- **Definition:**
  - Keep the test scripts and page interactions separate.
- **Example:**
  - Instead of having test logic mixed with element selectors, use methods defined in the page object.

<br>

**3. Reusability:**
- **Definition:**
  - Functions and methods can be reused across multiple tests.
- **Example:**
  - If multiple tests require logging in, the `loginPage.submit()` method can be reused.

---

### Structure

**1. Directory Setup:**
- **Folder Structure:**  
  <img src="https://github.com/rajneeshkumar1507/Cypress-Insights/blob/main/images/Screenshot%202024-10-28%20024423.png" alt="Folder Structure" width="600" />

<br>

**2. Example Page Object:** 
- **Login Page Object:**  
  <img src="https://github.com/rajneeshkumar1507/Cypress-Insights/blob/main/images/login-js.png" alt="Login Page Object" width="600" />

<br>

**3. Using Page Object in Tests**
- **Example Test File:**
  - **Login Tests**  
  <img src="https://github.com/rajneeshkumar1507/Cypress-Insights/blob/main/images/purchaseTest-cy-js.png" alt="Login Tests" width="600" />

---

### Advantages
**1. Maintainability**
  -  **Example:**
      - If the selector for the password input changes, update only the fillPassword method in the LoginPage object, not every test.
<br>

**2. Readability**
  -  **Example:**
      - Tests read like a story: loginPage.fillUsername('user') instead of cy.get('input[name="username"]').type('user'). <br>
<br>

**3. Refactoring**
  -  **Example:**
      - Change the login URL in the visit method, and all tests using it automatically get the update.
