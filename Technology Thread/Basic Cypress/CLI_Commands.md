# Basic CLI Commands

### Opening the Cypress Test Runner

The cypress open command is used to open the Cypress Test Runner, where you can interactively run and debug your tests.

```bash
cypress open
```

### Running Tests

The cypress run command is used to run Cypress tests headlessly, typically as part of your continuous integration (CI) pipeline.

```bash
cypress run
```

### Specifying a Browser

You can specify a browser to run your tests in using the --browser flag with the cypress run command.

```bash
cypress run --browser chrome
```

### Running Tests in Headless Mode

The cypress run --headless command is used to run tests in headless mode, without opening the Cypress Test Runner UI.

```bash
cypress run --headless
```

### Running Tests with Environment Variables

You can pass environment variables to your tests using the --env flag with the cypress run command.

```bash
cypress run --env foo=bar
```
