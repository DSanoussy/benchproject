
# TodoList Application

This is a Rust web application designed to manage multiple themed todo lists. Each list can contain tasks, and tasks can have various attributes such as tags, due dates, and priorities. The application is built using hexagonal architecture, ensuring that the core business logic is independent of external technologies.

## Folder Structure

- **src/**: Contains the source code, organized by the layers of the application.
- **migrations/**: Contains database migration files for setting up the schema.
- **tests/**: Contains integration tests for the application.
- **docker/**: Contains Docker-related files, including the `docker-compose.yml` file for setting up a PostgreSQL database.

## Setting Up the Development Environment

### 1. Cloning the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/yourusername/todolist-app.git
cd todolist-app
```

### 2. Setting Up the PostgreSQL Database

The application uses PostgreSQL as its database. You can set up the database using Docker. Instructions are provided in the `docker/` directory.

- Navigate to the [Docker Setup Guide](./docker/README.md) for detailed instructions on how to start and manage the PostgreSQL database using Docker.

### 3. Starting the PostgreSQL Database

To start the PostgreSQL database, navigate to the `docker/` directory and run:

```bash
docker compose up -d
```

The `-d` flag runs the container in detached mode, meaning it runs in the background.

### 4. Stopping the PostgreSQL Database

To stop the PostgreSQL database, use the following command:

```bash
docker compose down
```

This will stop the running container. The data will still be persisted in the `pgdata` volume.

### 5. Rebuilding or Updating the Database

If you need to update the PostgreSQL version or change environment variables, you can run:

```bash
docker compose up -d --build
```

This will rebuild the container with the new settings.

### 6. Building and Running the Application

To build and run the application, you need to have Rust installed. Follow the official Rust installation guide [here](https://www.rust-lang.org/tools/install).

Once Rust is installed, you can build the application with:

```bash
cargo build
```

And run it with:

```bash
cargo run
```

### 7. Running Tests

To run the integration tests, use the following command:

```bash
cargo test
```

## Contributing

If you wish to contribute to this project, please fork the repository and submit a pull request. We appreciate all contributions!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
