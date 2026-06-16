# GitHub Actions CI/CD Demo

![CI Pipeline](https://github.com/digimind34/github-actions-cicd-demo/actions/workflows/ci.yml/badge.svg)

## Overview

This project demonstrates a complete Continuous Integration and Continuous Deployment (CI/CD) pipeline using GitHub Actions, Python, Docker, and Docker Hub.

The pipeline automatically:

* Runs code quality checks with Flake8
* Executes automated tests using Pytest
* Builds a Docker image
* Authenticates with Docker Hub using GitHub Secrets
* Publishes the Docker image to Docker Hub

---

## Architecture

```text
Developer
    ↓
Git Push
    ↓
GitHub Repository
    ↓
GitHub Actions
 ├── Flake8 Linting
 ├── Pytest Testing
 ├── Docker Build
 └── Docker Push
    ↓
Docker Hub Repository

## Architecture

![Architecture Diagram](docs/architecture-diagram.png)
```

---

## Technologies Used

* GitHub Actions
* Python 3.12
* Pytest
* Flake8
* Docker
* Docker Hub

---

## Project Structure

```text
github-actions-cicd-demo
├── .github
│   └── workflows
│       └── ci.yml
├── app
│   ├── __init__.py
│   └── main.py
├── tests
│   ├── __init__.py
│   └── test_main.py
├── Dockerfile
├── requirements.txt
└── README.md
```

---

## CI/CD Pipeline Stages

### 1. Linting

```bash
flake8 .
```

Performs static code analysis and style validation.

### 2. Testing

```bash
pytest
```

Runs automated unit tests.

### 3. Docker Build

```bash
docker build -t github-actions-cicd-demo .

## Successful CI/CD Pipeline

![GitHub Actions Success](images/github-actions-success.png)
```

Builds the application container image.

### 4. Docker Push

```bash
docker push digi2/github-actions-cicd-demo:latest
```

Publishes the image to Docker Hub.

---

## Docker Hub Repository

```text
digi2/github-actions-cicd-demo
```

Pull the image:

```bash
docker pull digi2/github-actions-cicd-demo:latest
```

Run the image:

```bash
docker run digi2/github-actions-cicd-demo:latest

Docker Hub: [digi2/github-actions-cicd-demo](https://hub.docker.com/r/digi2/github-actions-cicd-demo)
```

---

## Skills Demonstrated

* Continuous Integration (CI)
* Continuous Deployment (CD)
* GitHub Actions Workflow Development
* Docker Containerization
* Docker Hub Image Publishing
* Secret Management
* Automated Testing
* Code Quality Automation

---

---
## Key Achievements

- Built an end-to-end CI/CD pipeline using GitHub Actions
- Automated Python testing and code quality validation
- Containerized applications using Docker
- Implemented secure secret management with GitHub Secrets
- Automated image publishing to Docker Hub
- Created reusable DevOps workflow templates
---

## Author

Babatunde Ayo

DevOps & Cloud Engineer

GitHub: [digimind34](https://github.com/digimind34)
