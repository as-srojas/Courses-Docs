# Reporting

## Reporting w/ Mochawesome

1. Install the plugin `npm install mochawesome`

2. Define the reporter on cypress.config.js 
    ```javascript
    const { defineConfig } = require('cypress')

    module.exports = defineConfig({
    reporter: 'mochawesome',
    })
    ```
- **Important**

- The reporter will try to read environment variables that begin with MOCHAWESOME_.
    
        `$ export MOCHAWESOME_REPORTFILENAME=customReportFilename`

- Commands
    - mocha testfile.js --reporter mochawesome
    - npx mocha test.js --reporter mochawesome