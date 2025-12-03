# 🚀 RapidStart-Express-NodeJS-WebApp-Template

This repository establishes a high-velocity, security-hardened boilerplate for modern Node.js web applications utilizing Express.js and EJS templating, optimized for immediate deployment via containerization (Docker/Codespaces).

## 🤖 AI Agent Directives (Mandatory Alignment)

<details><summary><strong>&#128734; APEX ARCHITECTURAL BLUEPRINT (DEC 2025)</strong></summary>

### 1. Identity & Prime Directive
**Role:** You are a Senior Principal Software Architect with **40+ years of elite industry experience**, enforcing FAANG-level standards. 
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof." 
**Output Standard:** Deliver **EXECUTION-ONLY** results based on the defined context.

### 2. Technology Stack Definition (Node.js/EJS)
*   **Language:** Node.js (LTS - v20+)
*   **Framework:** Express.js (v5+ adherence).
*   **Templating:** EJS (Encourage use of EJS Partial inclusion for componentization).
*   **Security:** OWASP Top 10 mitigation (Input Sanitization, CSRF Protection via **csurf**, Helmet usage).
*   **Database Abstraction:** Assume reliance on a modern ORM/ODM (e.g., Prisma or Mongoose), prioritizing clear **Port & Adapter (Hexagonal)** contracts for persistence layers.
*   **Containerization:** Docker Compose for local development environment definition.

### 3. Architectural & Coding Standards
*   **Patterns:** Enforce **SOLID Principles** rigidly. Ensure clear separation between Routes (Controller), Services (Business Logic), and Data Access Objects (DAO/Repository).
*   **DRY Principle:** Mandatory abstraction of repeated configuration logic (e.g., middleware loading, logger initialization).
*   **YAGNI:** Avoid over-engineering features not explicitly required by the current scope.
*   **Error Handling:** Implement centralized, structured error middleware to return consistent JSON error responses, preventing stack trace leakage.

### 4. Verification & Testing Commands
*   **Linting/Formatting (Biome Standard Applied):**
    bash
    npm run lint
    npm run format
    
*   **Unit Testing (Vitest/Jest Equivalent for Node):** Focus on service layer logic isolation.
    bash
    npm test:unit
    
*   **Integration Testing (Supertest/Playwright):** Verify full request/response cycles.
    bash
    npm test:integration
    
*   **Container Build Verification:**
    bash
    docker compose build --no-cache
    

</details>

## 🧭 Project Overview

BLUF: This repository provides an optimized Express.js and EJS template designed for rapid, secure deployment of full-stack web applications.

## 🏗️ Architecture Map (Simplified)

ascii
       +----------------------------------+
       |       Client (Browser/HTTP)      |
       +-----------------+----------------+
                         |
                         v
       +-----------------+----------------+
       |       Express Router/Controller  |
       |   (Input Validation, Auth)       |
       +-----------------+----------------+
                         |
                         v
       +-----------------+----------------+
       |        Application Services      |
       |   (Business Logic - Pure JS)     |
       +-----------------+----------------+
                         |
                         v
       +-----------------+----------------+
       |   Data Access Layer (Repositories)|
       |   (e.g., DB Connection Abstraction)|
       +-----------------+----------------+
                         |
                         v
       +-----------------+----------------+
       |        Persistent Storage (DB)   |
       +----------------------------------+

Views (EJS) are injected by the Controller layer based on Service outcomes.


## 📚 Table of Contents

1.  [🚀 RapidStart-Express-NodeJS-WebApp-Template](#-rapidstart-express-nodejs-webapp-template)
2.  [🤖 AI Agent Directives (Mandatory Alignment)](#-ai-agent-directives-mandatory-alignment)
3.  [🧭 Project Overview](#-project-overview)
4.  [🏗️ Architecture Map (Simplified)](#-architecture-map-simplified)
5.  [📚 Table of Contents](#-table-of-contents)
6.  [✨ Key Features](#-key-features)
7.  [⚙️ Technology Stack](#-technology-stack)
8.  [🛠️ Development Setup](#-development-setup)
9.  [📜 License](#-license)

## ✨ Key Features

*   **Production-Grade Security:** Pre-configured `helmet` middleware and CSRF protection.
*   **Containerized Ready:** Includes production-ready `Dockerfile` and `docker-compose.yml`.
*   **EJS Templating:** Standardized structure for views with robust partial management.
*   **Development Experience:** Configured for Hot Reloading/Nodemon during development.
*   **Codespaces Optimized:** Ready for instant cloud development environments.

## ⚙️ Technology Stack

| Component | Primary Technology | Version Standard |
| :--- | :--- | :--- |
| Runtime | Node.js | LTS (v20+)
| Web Framework | Express.js | v5+
| Templating Engine | EJS | Latest Stable
| Security | Helmet, csurf | Latest
| Formatting/Linting | Biome (Enforced) | Latest
| Testing | Vitest/Supertest | Latest
| Deployment | Docker | Latest

## 🛠️ Development Setup

Follow these steps to initialize the local development environment.

### Prerequisites
Ensure Node.js (v20+) and Docker are installed.

### Initialization
bash
git clone https://github.com/chirag127/RapidStart-Express-NodeJS-WebApp-Template.git
cd RapidStart-Express-NodeJS-WebApp-Template

# Use uv/npm/yarn/pnpm for dependency resolution
npm install

# Initialize environment variables (create .env from .env.example)
cp .env.example .env


### Execution Scripts

| Command | Description |
| :--- | :--- |
| `npm run dev` | Starts the application in development mode with hot reloading. |
| `npm run build` | Executes necessary production bundling (if any front-end assets were present; primarily for linting/security checks here). |
| `npm start` | Runs the optimized production build (via `node server.js`). |
| `npm test` | Runs combined unit and integration tests. |
| `npm run format` | Applies Biome formatting across all relevant files. |
| `docker compose up` | Builds and runs the application within the defined container environment. |

## 📜 License

This project is licensed under the **CC BY-NC 4.0 License**. See the [LICENSE](LICENSE) file for details.
