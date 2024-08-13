# `src/infrastructure/services/` Folder

This directory contains external service integrations, such as email providers or third-party APIs. These services are typically used by the application layer to perform operations that involve external systems.

## Example Services

- **email_notification_service.rs**: Handles sending email notifications to users, such as reminders when a task is due or notifications when a task is completed.
- **external_task_sync_service.rs**: Integrates with a third-party task management system to sync tasks across platforms, ensuring that tasks managed in this application can be reflected elsewhere (e.g., in a corporate task management tool).

Service implementations in this layer abstract the details of interacting with external systems, making it easier to change or replace these systems without affecting the core application logic.