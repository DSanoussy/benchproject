# `src/domain/` Folder

This directory contains the core business logic of the TodoList application, including entities, value objects, and repository interfaces. The domain layer represents the problem space of the application and should be free from dependencies on external technologies.

## Contents

- **entities/**: Contains the core business entities, which represent the main objects in your domain (e.g., `TodoList`, `Task`, `Tag`).
- **value_objects/**: Contains value objects that represent domain-specific concepts without unique identities, such as `Priority`, `DueDate`.
- **repositories/**: Contains abstract repository interfaces that define methods for interacting with the persistence layer, such as `TodoListRepository` or `TaskRepository`.

The domain layer is designed to be immutable, pure, and self-contained, allowing business rules to be clearly expressed and easily tested.
