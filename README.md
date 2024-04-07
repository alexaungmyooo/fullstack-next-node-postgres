# Full-Stack App with Next.js, Tailwind CSS, Node/Express, Prisma, PostgreSQL, Docker

This project is a simple yet complete full-stack application. It includes a frontend built with Next.js 14 and Tailwind CSS, a backend server using Node.js with Express, and a PostgreSQL database managed by Prisma. The entire stack is containerized using Docker and orchestrated with Docker Compose.

## Prerequisites

- Docker and Docker Compose
- Node.js (for local development)
- Yarn or npm (for managing JavaScript packages)

## Architecture Overview

- **Frontend**: Next.js 14 application with TypeScript, styled using Tailwind CSS.
- **Backend**: Node.js server with Express framework in JavaScript.
- **Database**: PostgreSQL, with schema and migrations managed by Prisma.
- **Containerization**: Docker for containerizing the application and Docker Compose for orchestration.

## Setup and Installation

1. **Clone the repository**

    ```bash
    git clone https://your-repository-url.git
    cd your-project-directory
    ```

2. **Environment Configuration**

    Copy the `.env.example` file to create a `.env` file. Adjust the database connection string and any other environment variables as necessary.

    ```bash
    cp .env.example .env
    ```

3. **Docker Compose**

    Use Docker Compose to build and run your containers. This will set up the Next.js frontend, the Express backend, and the PostgreSQL database.

    ```bash
    docker-compose up --build
    ```

    This command builds the images if they don't exist and starts the containers.

## Development

### Running Locally

For local development, you can run the frontend and backend outside of Docker if preferred. Ensure your PostgreSQL instance is accessible.

- **Backend (Express + Prisma)**

    Navigate to the backend directory, install dependencies, and run the development server:

    ```bash
    cd backend
    yarn install
    yarn dev
    ```

- **Frontend (Next.js + Tailwind CSS)**

    In a new terminal, navigate to the frontend directory, install dependencies, and start the Next.js development server:

    ```bash
    cd frontend
    yarn install
    yarn dev
    ```

### Accessing the Application

- The Next.js frontend will be available at [http://localhost:3000](http://localhost:3000).
- The Express backend API will be accessible at [http://localhost:4000](http://localhost:4000).

## Using Prisma

To manage your database schema, use Prisma migrations:

```bash
npx prisma migrate dev
```
This command creates a new migration based on your schema changes and applies it to the database.
