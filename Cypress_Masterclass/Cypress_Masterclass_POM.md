# Page Object Model
- A Design Principle
- Keep the objects & methods separate from tests scripts
-  Efficient reusability
- Easier, efficient and faster changes & maintenance

## Example 

- Directory Structure (Project dependent).
    ```javascript
    cypress/
    ├── fixtures/
    ├── e2e/
    │   ├── login.spec.js
    │   ├── dashboard.spec.js
    │   └── ...other_tests.spec.js
    ├── plugins/
    ├── support/
    └── pages/
        ├── LoginPage.js
        ├── DashboardPage.js
        └── ...other_page_objects.js
    ```
- Login.js
    ```javascript
    import LoginPage from '../pages/LoginPage';

    describe('Login Functionality', () => {
        beforeEach(() => {
            LoginPage.visit();
        });

        it('should log in with valid credentials', () => {
            LoginPage.fillUsername('your-username');
            LoginPage.fillPassword('your-password');
            LoginPage.submit();
        });

        it('should display an error message with invalid credentials', () => {
            LoginPage.fillUsername('invalid-username');
            LoginPage.fillPassword('invalid-password');
            LoginPage.submit();
        });
    });
    ```
- LoginPage.js
    ```javascript
    class LoginPage {
        visit() {
            cy.visit('/login');
        }

        fillUsername(username) {
            cy.get('[data-testid=username]').type(username);
        }

        fillPassword(password) {
            cy.get('[data-testid=password]').type(password);
        }

        submit() {
            cy.get('[data-testid=login-button]').click();
        }
    }

    export default new LoginPage();
    ```

- Also can define your elements in the PageObject For Example;
    ```javascript
        class LoginPage {
            usernameInput = '[data-testid=username]';
            passwordInput = '[data-testid=password]';
            loginButton = '[data-testid=login-button]';

            visit() {
                cy.visit('/login');
            }

            fillUsername(username) {
                cy.get(this.usernameInput).type(username);
            }

            fillPassword(password) {
                cy.get(this.passwordInput).type(password);
            }

            submit() {
                cy.get(this.loginButton).click();
            }
        }
        export default new LoginPage();
    ```
