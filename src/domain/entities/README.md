# `src/domain/entities/` Folder

This directory contains the core business entities of the TodoList application. These entities represent the main objects or concepts in your domain, each with a unique identity.

## Example Entities

- **todo_list.rs**: Represents a todo list, which contains a collection of tasks and is associated with a specific theme.
- **task.rs**: Represents a task within a todo list, which has attributes like `description`, `due_date`, `priority`, and `tags`.
- **tag.rs**: Represents a tag that can be associated with tasks to categorize them (e.g., `urgent`, `home`, `work`).

Entities encapsulate the state and behavior of the core business objects, following domain-driven design principles.
