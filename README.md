# CRUD API - Node.js

This project is a CRUD API built with Node.js and PostgreSQL, using Docker to simplify database setup.

## Requirements

Make sure you have the following applications installed:

- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/)

## Setting Up the Database with Docker

To start PostgreSQL using Docker, follow these steps:

1. **Pull the PostgreSQL image:**
   ```sh
   docker pull postgres
   ```

2. **Run the PostgreSQL container:**
   ```sh
   docker run --name postgres-db -e POSTGRES_PASSWORD=123 -p 5432:5432 -d postgres
   ```

3. **Access the database inside the container:**
   ```sh
   docker exec -it postgres-db psql -U postgres
   ```

4. **Create the database required for the application:**
   ```sql
   CREATE DATABASE crud;
   ```

Now the database is ready to be used by the application.

## Starting the API

1. Start the application:
   ```sh
   npm run dev
   ```

The API will be running and ready to receive requests.

---

For more information, check the official documentation for [PostgreSQL](https://www.postgresql.org/) and [Docker](https://docs.docker.com/).
