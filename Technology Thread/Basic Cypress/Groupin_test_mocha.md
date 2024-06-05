# Cypress_Mocha Grouping Tests

## Hooks

Cypress provides several hooks that allow you to run code at different stages of the test execution lifecycle. These hooks provide flexibility and customization options for your tests.

### before

The `before` hook runs once before all tests in a test suite. It is typically used to set up test data or perform other setup tasks that need to be done only once.

### beforeEach

The `beforeEach` hook runs before each test in a test suite. It is used to set up the test environment or reset any state that may have been modified during previous tests.

### afterEach

The `afterEach` hook runs after each test in a test suite. It is used to clean up the test environment or perform any teardown tasks that are necessary after each test.

### after

The `after` hook runs once after all tests in a test suite have finished executing. It is typically used to perform cleanup tasks or teardown operations that need to be done only once.

### skip

The `skip` hook allows you to skip a test or test suite. It is useful when you want to temporarily exclude certain tests from execution without deleting them from the codebase.

### only

The `only` hook allows you to run only the specified test or test suite, excluding all other tests. It is useful for focusing on a specific test during development or debugging, ignoring other tests.

### Example

```javascript
describe('Example Test Suite', () => {
  before(() => {
    // Runs once before all tests in the suite
    cy.log('Before All Tests');
  });

  beforeEach(() => {
    // Runs before each test in the suite
    cy.log('Before Each Test');
  });

  afterEach(() => {
    // Runs after each test in the suite
    cy.log('After Each Test');
  });

  after(() => {
    // Runs once after all tests in the suite
    cy.log('After All Tests');
  });

  it('Test 1', () => {
    cy.log('Test 1');
  });

  it.skip('Test 2 (Skipped)', () => {
    cy.log('Test 2');
  });

  it.only('Test 3 (Only)', () => {
    cy.log('Test 3');
  });
});
