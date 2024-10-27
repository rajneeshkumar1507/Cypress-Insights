## Page Object Model (POM) in Cypress: Detailed Notes with Examples
### Overview
- **POM**
  - A design pattern that enhances the maintainability and readability of test automation scripts.
- **Purpose**
  - Separates test logic from page-specific code, making tests cleaner and easier to manage.
<hr>

### Key Concept
**1. Page Objects:**
- **Definition:**
  - Classes or modules that represent individual pages or components of your application.
- **Example:**
  - For a login page, create a LoginPage object to manage all interactions with that page.
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
  - If multiple tests require logging in, the loginPage.submit() method can be reused.
 <hr>

 ### Structure
 **1. Directory Setup:**
 - **Folder Structure:**
  - ![](.)
 

