# Notes

## End-to-End testing

- Used to test the full stack intergration of the client and the server in a real browser environment.

- We want to verify that the common user path is functional with minimal mocking at the client, server or environment level

- We want to run the tests using an environment that matches production as closely as possible

## Cypres

- Each cypress command and their chains returns immediately.

- Cypress purposefully makes it so you **cannot** do anything useful with a return value.

- Avoid loops when writting tests with Cypress

- After test functions finish, Cypres executes the commands that were queued using cy.

- All cypress DOM based commands automatically wait for their elements to eist in the DOM. We **never** need to write .should('exist') after a dom based command
