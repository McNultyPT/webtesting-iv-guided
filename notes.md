# server testing

## components of an api

function name(args) => return something;

- routes/endpoints: url(data) => return response;
- business logic (validation/data conversion/operations).
- data access: talk to the persistent data store.

- set the test environment to run on 'node' instead of a browser
    - add to package.json 
    `"jest" : {
        "testEnvironment": "node"
    }
    `
    - make sure `cross-env` is installed as dev dependency

window => global

cross-env = npm package used to abstract away OS differences setting environment variables

DB_ENV=testing ===> DB_ENV=development in .env file

`npx knex migrate:latest --env=testing`

`yarn add supertest --dev`

- 
