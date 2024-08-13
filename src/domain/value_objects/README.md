# `src/domain/value_objects/` Folder

This directory contains value objects, which are immutable objects that represent domain-specific concepts. Unlike entities, value objects don't have a unique identity.

## Example Value Objects

- **priority.rs**: Represents the priority level of a task (e.g., `High`, `Medium`, `Low`).
- **due_date.rs**: Represents the due date for a task, including logic for validation and comparison.
- **task_status.rs**: Represents the status of a task (e.g., `Pending`, `Completed`, `InProgress`).

Value objects are used to encapsulate domain logic and ensure that concepts are correctly modeled and validated.
