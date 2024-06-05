# Writing Your First Test

## Assertions in Cypress

Assertions in Cypress are used to validate the expected behavior of your application. Cypress provides a rich set of built-in assertions that you can use to make sure that your application functions correctly.

## Common Assertions

- **`.should('exist')`**: Asserts that the element exists in the DOM.
- **`.should('be.visible')`**: Asserts that the element is visible.
- **`.should('have.text', 'expected text')`**: Asserts that the element has the expected text content.
- **`.should('have.value', 'expected value')`**: Asserts that the input element has the expected value.
- **`.should('have.attr', 'attribute', 'expected value')`**: Asserts that the element has the specified attribute with the expected value.
- **`.should('have.class', 'class-name')`**: Asserts that the element has the specified CSS class.

## Writing Your First Test in Cypress

Let's create a simple test to verify the functionality of a login form.

### Step 1: Navigate to the Login Page

```javascript
describe('Login Page', () => {
  it('should navigate to the login page', () => {
    cy.visit('/login') // Replace '/login' with the actual URL of your login page
  })
})
```

### Running Your Test

1. Save the test file with a .spec.js extension in the cypress/integration directory.

2. Open Cypress Test Runner by running npx cypress open in your terminal.

3. Click on the test file you created to run the test.
