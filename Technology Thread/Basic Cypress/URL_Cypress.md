# Cypress URL Commands

Cypress provides powerful URL commands that allow you to interact with URLs and perform various actions within your tests.

## Chromeweb security: False

By default, Cypress runs in a special browser environment where the same-origin policy and web security features are disabled. You can set `chromeWebSecurity` to `false` in your `cypress.json` file to disable web security, allowing your tests to interact with cross-origin content.

```json
{
  "chromeWebSecurity": false
}
```

## Main Describe Code

The main describe block in Cypress is where you define your test suite. It encapsulates all the tests and hooks related to a specific feature or functionality.

```javascript
describe('Cypress URL Commands', () => {
  // Tests and hooks go here
});
```

## Before Each-cy.visit

The beforeEach hook in Cypress is used to run code before each test in a test suite. You can use cy.visit() within the beforeEach hook to visit a specific URL before each test.

```javascript
beforeEach(() => {
  cy.visit('https://example.com');
});
```

### cy.title

The cy.title() command is used to retrieve the title of the current web page and make assertions based on it.

```javascript
it('should verify the title', () => {
  cy.title().should('include', 'Example');
});
```

### cy.url

The cy.url() command is used to retrieve the current URL of the web page and make assertions based on it.

```javascript
it('should verify the URL', () => {
  cy.url().should('eq', 'https://example.com');
});
```

### cy.location: protocol
The cy.location() command is used to retrieve information about the current URL, such as the protocol.

```javascript
it('should verify the protocol', () => {
  cy.location('protocol').should('eq', 'https:');
});
```

### cy.location: hostname

The cy.location() command is used to retrieve information about the current URL, such as the hostname.

```javascript
it('should verify the hostname', () => {
  cy.location('hostname').should('eq', 'example.com');
});
```

### cy.location: pathname

The cy.location() command is used to retrieve information about the current URL, such as the pathname.

```javascript
it('should verify the pathname', () => {
  cy.location('pathname').should('eq', '/');
});
```

### Selectors, Type And Click

Cypress provides commands like cy.get(), cy.type(), and cy.click() to interact with elements on the page using CSS selectors.

```javascript
it('should interact with elements', () => {
  cy.get('#username').type('user123');
  cy.get('#password').type('pass123');
  cy.get('.submit-button').click();
});
```
