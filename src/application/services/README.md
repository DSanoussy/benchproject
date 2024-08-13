# `src/application/services/` Folder

This directory contains the application services, which are responsible for implementing the business logic and coordinating actions between the domain and infrastructure layers.

## Example Services

- **todo_list_service.rs**: Handles operations related to creating, updating, and retrieving todo lists.
- **task_service.rs**: Manages tasks within todo lists, including operations like adding, updating, and deleting tasks.
- **tag_service.rs**: Manages tags that can be associated with tasks, including creating and assigning tags.

Each service interacts with one or more domain entities and repositories to fulfill its responsibilities.
