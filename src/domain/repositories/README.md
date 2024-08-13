# `src/domain/repositories/` Folder

This directory contains repository interfaces, which define methods for interacting with the persistence layer (e.g., databases). These interfaces are implemented in the infrastructure layer.

## Example Repositories

- **todo_list_repository.rs**: Defines the methods for interacting with the todo list data store, such as `find_by_id`, `save`, and `delete`.
- **task_repository.rs**: Defines the methods for interacting with the task data store, such as `find_by_list_id` and `update`.
- **tag_repository.rs**: Defines the methods for managing tags in the persistence layer.

Repositories abstract the data access logic and allow the domain layer to remain decoupled from the specifics of the persistence technology.
