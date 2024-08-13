
# Docker Setup for PostgreSQL

This `docker-compose.yml` file is designed to quickly set up a PostgreSQL database using Docker. Docker Compose simplifies the process of managing the database container, ensuring that the environment is consistent across different machines and easy to reproduce.

## Services

### 1. `postgresql`
- **Image**: `postgres:16.3`
    - This service uses the official PostgreSQL Docker image, specifically version 16.3.
- **Environment Variables**:
    - `POSTGRES_DB`: The name of the default database that will be created when the container starts.
    - `POSTGRES_USER`: The default PostgreSQL user.
    - `POSTGRES_PASSWORD`: The password for the `POSTGRES_USER`.
- **Ports**:
    - `5434:5432`: Maps port 5434 on the host machine to port 5432 in the container, which is the default port for PostgreSQL. This allows you to connect to the PostgreSQL database using `localhost:5434`.
- **Volumes**:
    - `pgdata:/var/lib/postgresql/data`: This mounts a named Docker volume (`pgdata`) to the PostgreSQL data directory inside the container, ensuring that your database data is persisted across container restarts and recreations.

## Volumes

### 1. `pgdata`
- This is a named volume used to persist the PostgreSQL data. Even if the container is removed, the data stored in this volume will remain intact, allowing you to bring the database back up without losing any information.

## How to Use

### 1. Start the Database
To start the PostgreSQL database, run the following command in the directory containing the `docker-compose.yml` file:

```bash
docker compose up -d
```

The `-d` flag runs the container in detached mode, meaning it runs in the background.

### 2. Access the Database
You can connect to the PostgreSQL database using any PostgreSQL client (e.g., `psql`, DBeaver, or PgAdmin) with the following connection details:

- **Host**: `localhost`
- **Port**: `5434`
- **Database**: The name specified in `POSTGRES_DB`
- **User**: The user specified in `POSTGRES_USER`
- **Password**: The password specified in `POSTGRES_PASSWORD`

### 3. Stop the Database
To stop the PostgreSQL database, use the following command:

```bash
docker compose down
```

This will stop the running container. The data will still be persisted in the `pgdata` volume.

### 4. Rebuild or Update the Database
If you need to update the PostgreSQL version or change environment variables, you can run:

```bash
docker compose up -d --build
```

This will rebuild the container with the new settings.

## Notes

- This setup is intended for development purposes. In a production environment, you may want to use different environment variables, especially for the `POSTGRES_PASSWORD`, and consider using a managed database service for better security and scalability.
- The `docker-compose.yml` file and associated configurations are designed to be simple and easy to understand, making it ideal for getting started with PostgreSQL in a development environment.
