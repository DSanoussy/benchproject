# `src/` Folder

This directory contains the source code for the TodoList application, structured according to hexagonal architecture principles. The code is organized into the following subdirectories:

- **application/**: Contains the application services and use cases that coordinate the core business logic.
- **domain/**: Contains the core business entities, value objects, and repository interfaces that represent the core of the application.
- **infrastructure/**: Contains implementations of repository interfaces and integrations with external systems like databases and messaging services.
- **interfaces/**: Contains the HTTP interface, where external requests are handled and routed to the appropriate application services.

Each subdirectory contains a `README.md` file explaining its specific role and the types of files it contains.
