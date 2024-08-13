# `src/tests/` Folder

This directory contains integration tests for the application. Integration tests ensure that the various components of the application work together as expected.

## Example Tests

- **integration_test.rs**: Contains tests that verify the integration between different layers of the application, such as testing that tasks can be added to a todo list, or that users can retrieve their lists and tasks through the API.
- **database_test.rs**: Contains tests that verify the interaction between the application and the database, ensuring that data is correctly persisted and retrieved.

The tests in this folder help maintain the integrity of the application as it evolves, ensuring that new changes do not break existing functionality.
