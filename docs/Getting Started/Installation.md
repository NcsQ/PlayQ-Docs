---
sidebar_position: 1
---

# Installation

## Setup:
1. Clone or download the project
2. Extract and open in the VS-Code
3. npm i to install the dependencies
4. npx playwright install to install the browsers
5. npm run test to execute the tests
6. To run a particular test change
    ``` 
    paths: [
            "src/test/features/featurename.feature"
         ] 
    ```
7. Use tags to run a specific or collection of specs
    ```
    npm run test --TAGS="@test or @add"
    ```