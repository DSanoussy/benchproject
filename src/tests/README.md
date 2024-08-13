
# Integration Tests

This directory contains integration tests for the application. These tests ensure that all layers of the application work together as expected, including interactions with external services like PostgreSQL.

## Structure

- **support/**: Contains shared setup code for Testcontainers, which is used across multiple tests.
  - **mod.rs**: Module file that exposes the setup functions.
  - **testcontainers_setup.rs**: Contains the setup logic for Testcontainers.
- **integration_test.rs**: Example integration test using the shared Testcontainers setup.

## Running Tests

To run all integration tests, use the following command:

```bash
cargo test
```

This command will execute all tests in this directory, spinning up and tearing down Docker containers as required.

## Testcontainers

The integration tests make use of Testcontainers to spin up real instances of external services like PostgreSQL. This ensures that the tests are as close to real-world scenarios as possible. The setup for these containers is handled in the `support/` module, allowing it to be reused across multiple tests.
