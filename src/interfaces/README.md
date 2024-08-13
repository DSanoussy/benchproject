# `src/interfaces/` Folder

This directory contains the HTTP and CLI interfaces, which handle external requests and route them to the appropriate application services. The interfaces layer is the entry point for external interactions with the application.

## Contents

- **http/**: Contains the HTTP-related code, including route definitions and request handlers. This is where the application exposes its functionality as a web service.
- **cli/**: Contains command-line interface (CLI) related code, allowing users to interact with the application through a terminal.
- **routes/**: Organizes the routing logic, which maps incoming HTTP requests to the appropriate handlers.

The interfaces layer is responsible for translating external requests into the appropriate application service calls, ensuring that the core business logic is executed in response to these interactions.
