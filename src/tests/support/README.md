
# Testcontainers Support Module

This directory contains the shared setup code for Testcontainers, which is used across multiple integration tests. The goal is to provide a reusable context for tests that require external services like databases.

## Files

- **mod.rs**: Module file to expose the setup functions.
- **testcontainers_setup.rs**: Contains the setup logic for Testcontainers, including functions to start Docker containers and provide connection strings.

## Usage

In your integration tests, you can use the shared setup like this:

```rust
use crate::support::testcontainers_setup::setup_testcontainers;

#[tokio::test]
async fn test_example() {
    let context = setup_testcontainers().await;

    // Use the context to interact with the database, etc.
}
```

## Benefits

- **Reusability**: Avoids duplicating setup code across tests.
- **Consistency**: Ensures all tests run against the same environment setup.
- **Ease of Maintenance**: Changes to container configurations only need to be made in one place.
