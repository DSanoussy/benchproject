# `src/infrastructure/database/` Folder

This directory contains the database-related code, including implementations of repository interfaces and database connection management.

## Example Implementations

- **postgres_todo_list_repository.rs**: Implements the `TodoListRepository` interface using a PostgreSQL database.
- **postgres_task_repository.rs**: Implements the `TaskRepository` interface using a PostgreSQL database.
- **postgres_tag_repository.rs**: Implements the `TagRepository` interface using a PostgreSQL database.

The database layer abstracts the specifics of how data is stored and retrieved, allowing the core application to remain agnostic to the underlying technology.
