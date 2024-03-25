# Mocha Javascript Framework
A testing framework for organize and execute cases for Asynchronous testing to be a simple way.

### Install
- Install NodeJs
- Install Npm
- Just create a project and run the following command: `npm install mocha` and confirm the correct installation with `mocha --version`.

### Pre-Boundled Function Calls

#### Describe

The describe function in Mocha is utilized for grouping related tests together, effectively creating test suites.

It requires two parameters: a string that describes the test suite, and a callback function that contains the individual tests.


```javascript

    describe('Test', function() {
      describe('#indexOf()', function() {

      });
    });
```
#### it

The it function is employed for defining individual test cases or specifications.

It takes a string that describes the specific behavior being tested and a callback function containing the test assertions.


```javascript
    it('should return -1 when the value is not present', function() {
      // Test assertions go here
    });
```

### Mocha Hooks

#### Before and After Hooks

Mocha provides before and after hooks to execute setup and teardown tasks before and after running tests, respectively. These hooks are useful for operations like database setup, server initialization, etc.

The before and after functions accept a callback function that will be executed before/after all tests in the suite.

```javascript
    before('Hook Description', function() {
        // Runs before all tests in the suite
    });

    after('Hook Description', function() {
        // Runs after all tests in the suite
    });
```
#### Before Each and After Each Hooks

Mocha also offers beforeEach and afterEach hooks to execute setup and teardown tasks before and after each individual test, respectively.
The beforeEach and afterEach functions take a callback function that will be executed before/after each test in the suite.

```javascript
beforeEach('Hook Description', function() {
  // Runs before each test in the suite
});

afterEach('Hook Description', function() {
  // Runs after each test in the suite
});
```

### Test Features - Inclusive, Exclusive and Pending

Test features refer to the functionalities or aspects of your software that you want to test. These can range from basic unit tests for individual functions to comprehensive integration tests for entire modules or systems.

```javascript
describe('Login Feature', function() {
  it('should allow users to login with valid credentials', function() {
    // Test logic for valid login
  });

  it('should display an error message for invalid credentials', function() {
    // Test logic for invalid login
  });
});
```

#### Inclusive Test

Inclusive tests are those that are included or executed as part of the test suite. These tests are intended to verify expected behaviors and ensure the correctness of the software.
  
Inclusive tests are written using it statements within a describe block and are executed alongside other tests.

```javascript
describe('Test Suite', function() {
  it('Run Normally Test', function() {

  });
});
```
#### Exclusive Test

Exclusive tests are those that are intentionally excluded or skipped from the test suite. This might be due to incomplete implementation, known issues, or specific test configurations.
  
Exclusive tests are written using it.skip or it.only statements to skip or exclusively run specific tests, respectively.

```javascript
describe('Test Suite', function() {
  it.skip('Skip Test', function() {

  });

  it.only('Only Run This Test', function() {

  });
});
```
#### Pending Tests

Pending tests are placeholders for tests that have not been implemented yet. They serve as a reminder to add test cases for certain functionalities or behaviors in the future.
  
Pending tests are created by using it statements without a callback.

```javascript
describe('Test Pending', function() {
  it('should do something (pending)');
});
```
### Retry & Timeout Functions

#### Retry Functionality

Retry functionality in Mocha allows you to rerun failed tests a certain number of times before marking them as failed. This can be helpful in dealing with flaky tests that occasionally fail due to external factors.

Retry functionality can be implemented using third-party plugins or custom code to define how many times a test should be retried and under what conditions.
    

```javascript
//Example (using mocha-retry plugin)
    const retry = require('mocha-retry');

    describe('Test', function() {
      retry(3).it('should pass eventually', function() {
        // Test logic that may fail
      });
    });
```

#### Timeout Functionality

Timeout functionality in Mocha allows you to set a maximum time limit for each test case to complete execution. If a test exceeds this time limit, it will be marked as failed.

Timeout functionality can be set globally for all tests or individually for specific tests using the this.timeout() function or the timeout option in the describe or it functions.

```javascript
describe('Test Suite', function() {
  //Set timeout for all tests in this suite
  this.timeout(5000);

  it('should not exceed the specified time limit', function(done) {

    setTimeout(done, 4000); //Finish the test after 4 seconds
  });

  it('should pass within the specified time limit', function(done) {
    // Test logic that should complete quickly
    setTimeout(done, 2000); 
  }).timeout(3000); // Override timeout for this specific test
});
```

### Reporters - Spec and Dot Matrix
#### Types
**SPEC** - This is the default reporter. Outputs a hierarchical view according to the tests cases.

**DOT MATRIX** - Is a series of characters which represent the Tests Cases. Failures are highlighted in red exclamation marks, pending with a blue comma, and slow tests as yellow.

**Other Types**  - NYAN, TAP, Landing Strip, Progress, JSON, JSON Stream, Min, Doc.

#### Commands

You should run the following commmand to create a Report 
- 'mocha test/ --reporter spec'
- 'mocha test/ --reporter dot'
- 'mocha test/ --reporter json'