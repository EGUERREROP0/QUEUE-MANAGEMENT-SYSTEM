# Queue Management System

A queue management system built with a monorepo architecture using **pnpm workspaces**.

## Project Structure

```text
queue-management-system/
│
├── frontend/             # Frontend application
├── backend/              # Backend API / server
├── package.json          # Root configuration
├── pnpm-workspace.yaml   # Workspace configuration
├── pnpm-lock.yaml
└── README.md
```

## Tech Stack

### Frontend

* React
* Vite

### Backend

* Node.js
* Express

### Package Manager

* pnpm

## Requirements

Make sure you have installed:

* Node.js 20+
* pnpm

Check versions:

```bash
node -v
pnpm -v
```

## Installation

Clone the repository:

```bash
git clone <repository-url>
cd queue-management-system
```

Install all dependencies:

```bash
pnpm install
```

This command installs dependencies for:

* Root workspace
* Frontend
* Backend

## Running the Project

Start frontend and backend together:

```bash
pnpm dev
```

Default ports:

* Frontend: http://localhost:5173
* Backend: http://localhost:3001

## Available Scripts

### Root

Run both frontend and backend:

```bash
pnpm dev
```

### Frontend

Run frontend only:

```bash
pnpm --filter frontend dev
```

Build frontend:

```bash
pnpm --filter frontend build
```

### Backend

Run backend only:

```bash
pnpm --filter backend dev
```

## Workspace Configuration

The project uses `pnpm-workspace.yaml`:

```yaml
packages:
  - 'frontend'
  - 'backend'
```

This allows pnpm to manage both applications within a single repository.

## Git Ignore

Recommended `.gitignore`:

```gitignore
node_modules
dist
.env
```

`node_modules` are not committed to Git. They are recreated with:

```bash
pnpm install
```

## License

MIT
