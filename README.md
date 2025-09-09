# DockerizeAngularApp

A simple Angular application demonstrating how to containerize an Angular app with Docker.

## About

This project contains a basic Angular application (built with Angular CLI 20.1.0) that has been configured to run in a Docker container using NGINX as the web server.

## Docker Setup

### Build the Docker Image

```bash
docker build -t dockerize-angular-app .
```

### Run the Container

```bash
docker run -d -p 4200:8080 --name helpdesk dockerize-angular-app
```

The application will be available at `http://localhost:4200`

### Stop the Container

```bash
# Find the container ID
docker ps

# Stop the container
docker stop <container-id>
```

## Local Development

For local development without Docker:

```bash
npm install
ng serve
```

Open `http://localhost:4200` in your browser.
