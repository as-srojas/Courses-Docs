# Validation

## Using setTimeout in Cypress Test Example

Suppose you have a scenario where you want to wait for a certain condition to be met before proceeding with the test. In this example, let's wait for 2 seconds before asserting the visibility of an element.

```javascript
describe('Custom Wait Strategy', () => {
  it('should wait for 2 seconds before asserting visibility', () => {
    cy.visit('https://example.com');
    cy.get('.reveal-button').click();
    cy.wait(2000);
    cy.get('.visible-element').should('be.visible');
  });
});
```

```javascript
describe('Custom Wait Strategy', () => {
  it('should wait for 2 seconds before asserting visibility', () => {
    cy.visit('https://example.com');
    cy.get('.reveal-button').click();

    setTimeout(() => {
      cy.get('.visible-element').should('be.visible');
    }, 2000);
  });
});
```
