DevOps Test Project

This repository demonstrates a complete DevOps workflow including CI/CD pipeline automation, Dockerized application deployment, and multi-service orchestration using Docker Compose.

Repository URL

https://github.com/madhupratika27-code

Features

CI/CD Pipeline

Automatically builds, tests, and validates the app on every push using a GitHub workflow.

Ensures that the application is always in a deployable state.

Dockerized Application

The app is containerized using Docker for consistent runtime environments.

Dockerfile provided for building the app image.

Docker Compose Multi-Service Deployment

Orchestrates multiple services including the application and its dependencies.

Simplifies local environment setup with a single docker-compose up command.

Getting Started
Prerequisites

Docker

Docker Compose

Git

Clone the Repository
git clone https://github.com/madhupratika27-code/devops-test.git
cd devops-test

Build and Run with Docker Compose
docker-compose up --build


The app will start in a container.

Access the app via http://localhost:3000 

Pipeline Workflow

Code Push
Every push to the GitHub repository triggers the CI/CD pipeline.

Build Stage

Docker image of the app is built.

Dependencies are installed, and environment validation is performed.

Test Stage

Application tests run automatically.

Pipeline ensures code quality before deployment.

Deploy Stage

The Docker Compose configuration starts all required services.

App is ready to run locally or in a target environment.

Folder Structure
devops-test/
│
├── Dockerfile          # Docker configuration for the app
├── docker-compose.yml  # Docker Compose setup for multi-service deployment
├── Jenkinsfile         # Pipeline definition (if used)
├── src/                # Application source code
├── package.json        # Node.js app dependencies
└── README.md           # Project documentation

Additional Notes

Ensure Docker and Docker Compose are running before executing commands.

The CI/CD workflow can be easily extended to integrate Kubernetes, Prometheus, or Grafana for monitoring in future iterations.

This repository is designed for educational and assessment purposes, demonstrating DevOps best practices.
