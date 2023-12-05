# What are App Actions

- Shortcuts in app
- Provide users with quick ways to navigate to specific activities in app change the state of your app without user interactions (GUI).

# Read And Write Files w/ Cypress
Json For Examples 
```json
    {
        "username": "testuser",
        "password": "testpassword"
    }
```
- Using Fixture
    ```javascript
        cy.fixture('example').then((data) => {
        cy.get('#username').type(data.username);
        cy.get('#password').type(data.password);
        });
    ```

- Using readFile
    ```javascript
        cy.readFile('log.txt').then((content) => {
            console.log(content);
        });
    ```

- Using writeFile
    ```javascript
        const dataToWrite = 'This is some data to write to a file.';
        cy.writeFile('output.txt', dataToWrite);
    ```

- Using Cypress-Upload-File

    You need the plugin: 
    `npm install --save-dev cypress-file-upload`

    ```javascript
        import 'cypress-file-upload';

        describe('File Upload Test', () => {
            it('should upload a file', () => {
                cy.visit('your_upload_page_url');

                const fileName = 'example.jpg'; 

                cy.get('#uploadImage').attachFile('fileName');
            });
        });
    ```

- Using Cypress-Download-File
    1. You need the plugin `npm install cypress-downloadFile`

    2. Add the following line to cypress/support/commands.js.    
    `require('cypress-downloadfile/lib/downloadFileCommand')`

    3. Add the following lines to cypress.config.js.

        ```javascript
            const { defineConfig } = require("cypress");
            const {downloadFile} = require('cypress-downloadfile/lib/addPlugin')

            module.exports = defineConfig({
            retries: {runMode: 2, openMode: 0},
            e2e: {
                setupNodeEvents(on, config) {
                // implement node event listeners here
                    on('task', {downloadFile}) //This line
                },
            },
            });
        ```
    
        4. Add the following lines to cypress/plugins/index.js.

        ```javascript
            const {downloadFile} = require('cypress-downloadfile/lib/addPlugin')
            module.exports = (on, config) => {
                on('task', {downloadFile})
            }
        ```

        5. Example
            `cy.downloadFile('https://upload.wikimedia.org/wikipedia/en/a/a9/Example.jpg','mydownloads','example.jpg')`