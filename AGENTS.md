# MetaMCP Project: Agents Context

This document provides a comprehensive overview of the MetaMCP project, designed to be used as a context file for Agents.

## Project Overview

MetaMCP is a monorepo project that provides a MCP (Model Context Protocol) proxy server. It allows you to aggregate multiple MCP servers into a single endpoint, and apply middleware to the requests and responses. The project is built with a modern tech stack, including:

*   **Frontend:** Next.js, React, TypeScript
*   **Backend:** Node.js, Express.js, tRPC
*   **Database:** PostgreSQL
*   **Monorepo:** Turborepo
*   **Containerization:** Docker

The project is divided into two main applications: `frontend` and `backend`. The `frontend` is a Next.js application that provides the user interface for managing MCP servers, namespaces, and endpoints. The `backend` is an Express.js application that provides the core functionality of the MCP proxy, including authentication, tRPC API, and the MCP proxy itself.

## Building and Running

The project uses `pnpm` as the package manager. To get started, you need to install the dependencies:

```bash
pnpm install
```

### Development

To run the project in development mode, you can use the following command:

```bash
pnpm dev
```

This will start both the `frontend` and `backend` applications in development mode. The frontend will be available at `http://localhost:12008`, and the backend will be available at `http://localhost:12009`.

Alternatively, you can use Docker Compose to run the project in a containerized environment:

```bash
pnpm dev:docker
```

This will start the `frontend`, `backend`, and `postgres` services in Docker containers.

### Production

To build the project for production, you can use the following command:

```bash
pnpm build
```

This will create a production-ready build of both the `frontend` and `backend` applications.

To run the project in production, you can use Docker Compose:

```bash
docker compose up -d
```

This will start the `app` and `postgres` services in Docker containers. The application will be available at `http://localhost:12008`.

## Development Conventions

The project follows a set of development conventions to ensure code quality and consistency.

### Linting and Formatting

The project uses ESLint for linting and Prettier for formatting. You can run the following commands to check and fix your code:

```bash
pnpm lint
pnpm lint:fix
pnpm format
```

### Type Checking

The project uses TypeScript for static type checking. You can run the following command to check for type errors:

```bash
pnpm check-types
```

### Testing

TODO: Add information about the testing practices and commands.
