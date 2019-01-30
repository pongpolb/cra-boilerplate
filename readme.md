# Table of Contents

- [Project Structure](#project-structure)

## Project Structure

- **[MUST]** Follow folder structure

    ```
    src/
      /components         - stateless components used across the application
      /config             - configuration files separated layer by each environment
      /helpers            - High order components such as Redux setup, Authorization
                            also utilities functions

      /modules            - modules will contains each function related to that resources
        /:resources_name
          /actions        - functions related to this resouces
          /components     - stateful components specificly only this resources
          /constants      - constants for this resource
          /reducers       - reducers related to actions
          /sagas          - sagas hook related to actions
          /selectors      - selectors for this resources

      /static
        /css              - css files
        /fonts            - fonts
        /images           - favicons, logo
        /locales          - localization files

      routes.js           - router files
      reducer.js          - root reducer
      saga.js             - root saga
      store.js            - store file
      index.js(entry.js)  - entry point of react app

    test/
      /storybook          - components test
      /integration        - web application functional test

    ```