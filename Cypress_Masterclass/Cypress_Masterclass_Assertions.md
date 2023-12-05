# Cypress Notes
- **Important** In each case you can use: Only, BeforeEach and Skip statements for order of execution.
- `cy.get()` : Used to select elements directly on the page.
- `cy.find()` : Used to search for elements within a parent or container element.

## Implicit Assertions
- should-contain

    Example: 
    ```javascript
    .should.('contain', 'Button')
    ```
- should-have

    Example: 
    ```javascript
    .should.('have.class', 'query-btn')
    ```
    -- **have.text, have.html**
- should-be

    Example: 
    ```javascript
    .should.('be.visible')
    .should.('be.selected')
    .should.('be.disabled')
    .should.('be.focused') equivalent to .should('have.focus')
    ```
    
- should-equal
    
    Example: 
    ```javascript
    .invoke('attr','id').should('equal', 'query-btn')
    ```
- and
    Example: 
    ```javascript
    .should.('have.class', 'query-btn').and('contain', 'Button')
    ```
    **Chained Assertions**

## Explicit Assertions
- expect

    Example: 
    ```javascript
    expect(true).to.be.true

    let name = 'cypress'
    expect(name).to.be.equal('cypress')
    ```

- assert 
    
    Example: 
    ```javascript
        assert.equal
        assert.notEqual
    ```