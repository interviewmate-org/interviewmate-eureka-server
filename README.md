# Eureka Server - InterviewMate Platform

Service Registry for the InterviewMate Microservices Ecosystem.

---

## Overview

The Eureka Server acts as the central service discovery component of the InterviewMate distributed architecture. It enables microservices to dynamically register themselves and discover other services without hardcoded network configurations.

This repository is part of the InterviewMate platform engineering initiative focused on scalable, cloud-native, and containerized microservice architecture.

---

## Tech Stack

* Java 21
* Spring Boot 3
* Spring Cloud Netflix Eureka
* Maven
* Docker
* GitHub Container Registry (GHCR)

---

## Features

* Centralized service registration
* Dynamic service discovery
* Microservice health awareness
* Container-ready deployment
* Multi-stage optimized Docker build
* Non-root container execution
* Lightweight runtime image

---

## Project Structure

```plaintext
eureka-server/
│
├── .github/
│   └── workflows/
│
├── src/
│   ├── main/
│   └── test/
│
├── Dockerfile
├── .dockerignore
├── pom.xml
├── README.md
├── mvnw
└── mvnw.cmd
```

---

## Running Locally

### Clone Repository

```bash
git clone https://github.com/interviewmate-org/interviewmate-eureka-server.git
cd eureka-server
```

---

### Build Application

Linux / Mac:

```bash
./mvnw clean package
```

Windows:

```bash
mvnw.cmd clean package
```

---

### Run Application

```bash
java -jar target/*.jar
```

---

## Access Eureka Dashboard

```plaintext
http://localhost:8761
```

---

## Docker Setup

### Build Docker Image

```bash
docker build -t eureka-server .
```

---

### Run Docker Container

```bash
docker run -p 8761:8761 eureka-server
```

---

## Docker Architecture

The Docker image uses:

* Multi-stage build optimization
* Maven dependency caching
* Slim Java runtime container
* Non-root execution model
* Optimized JVM runtime configuration

---

## Branching Strategy

| Branch    | Purpose                |
| --------- | ---------------------- |
| main      | Production-ready code  |
| develop   | Active development     |
| feature/* | Feature implementation |

---

## Versioning Strategy

This project follows Semantic Versioning.

Examples:

```plaintext
1.0.0-SNAPSHOT
1.0.0-rc1
1.0.0
```

| Version Type | Meaning            |
| ------------ | ------------------ |
| SNAPSHOT     | Development build  |
| rc           | Release candidate  |
| stable       | Production release |

---

## CI/CD Pipeline

GitHub Actions pipeline automatically performs:

* Maven build
* Test execution
* Docker image build
* GHCR image publishing
* Version tagging
* Artifact generation

---

## Container Registry

Docker images are published to:

```plaintext
ghcr.io/interviewmate/eureka-server
```

---

## Security Practices

* Non-root container user
* Lightweight runtime image
* Minimal attack surface
* Dependency isolation
* CI-based validation

---

## Future Enhancements

* Kubernetes deployment
* Helm chart support
* Prometheus monitoring
* Grafana dashboards
* Distributed tracing
* Centralized logging
* Service mesh integration

---

Project Initiative: InterviewMate - AI Powered Interview Preparation System 

---

## License

This project is currently proprietary and intended for the InterviewMate platform ecosystem.
