
# `src/` Folder

This directory contains the source code for the TodoList application, structured according to hexagonal architecture principles. The code is organized into the following subdirectories:

- **application/**: Contains the application services and use cases that coordinate the core business logic.
- **domain/**: Contains the core business entities, value objects, and repository interfaces that represent the core of the application.
- **infrastructure/**: Contains implementations of repository interfaces and integrations with external systems like databases and messaging services.
- **interfaces/**: Contains the HTTP and CLI interfaces, where external requests are handled and routed to the appropriate application services.

Each subdirectory contains a `README.md` file explaining its specific role and the types of files it contains.

## Integration Testing

Integration tests are placed in the `tests/` directory at the root of the project. These tests make use of Testcontainers to spin up real instances of external services (like PostgreSQL) during the test process. The configuration and setup for Testcontainers are centralized in the `tests/support/` module, ensuring that the setup is consistent and reusable across multiple tests.

### Running Tests

To run integration tests, use the following command from the project root:

```bash
cargo test
```

This will execute all tests in the `tests/` directory, including those that use Testcontainers.

## Folder Structure

- **application/**: Handles business logic coordination.
- **domain/**: Core business entities and rules.
- **infrastructure/**: Integrations with external systems and repositories.
- **interfaces/**: HTTP and CLI interfaces for external interaction.

The structure is designed to keep the core business logic independent of external technologies, ensuring maintainability and testability.
