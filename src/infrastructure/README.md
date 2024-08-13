# `src/infrastructure/` Folder

This directory contains implementations of repository interfaces, as well as integrations with external systems like databases and messaging services. The infrastructure layer serves as the adapter between the core business logic and the outside world.

## Contents

- **database/**: Contains the database-related code, such as repository implementations and database connection management.
- **messaging/**: Contains the code related to messaging systems like RabbitMQ for asynchronous operations.
- **services/**: Contains external service integrations, such as email notifications or third-party task management APIs.

The infrastructure layer handles the technical details, allowing the core application to remain focused on business logic.
