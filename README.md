# Comprehensive Jenkins Project 

This repository contains a step-by-step progression for learning Jenkins and building continuous integration and continuous deployment (CI/CD) pipelines. Each directory in the repository represents a progressively advanced stage of automating software delivery using Jenkins.

## Project Structure & Progression

### 1. `01-jenkins-basics`
- **Focus:** Jenkins Pipeline Fundamentals.
- **Details:** Introduces the fundamental concepts of declarative Jenkins pipelines. It includes a simple Python Flask application (`app.py`), a suite of unit tests (`test_app.py`), and a standard `Jenkinsfile` for downloading, building, and automatically testing the code.

### 2. `02-single-server-deployment`
- **Focus:** Deploying to a Single Server (EC2/VM).
- **Details:** Expands the basic pipeline to actually deploy the application to a running server. The `Jenkinsfile` is expanded to manage configuring the environment and deploying the application onto a single target machine, simulating simple infrastructure deployment.

### 3. `03-lambda-deployment`
- **Focus:** AWS Serverless Deployment.
- **Details:** Shifts the deployment paradigm from a traditional VM to Cloud Serverless architecture. It includes necessary AWS IAM policies (`iam-policy.json`) and deploys a serverless version of the application directly to AWS Lambda through the Jenkins pipeline.

### 4. `04-docker`
- **Focus:** Containerization.
- **Details:** Introduces Docker to standardise the application environment. The Jenkins pipeline now packages the Flask application into a Docker container via the included `Dockerfile`, demonstrating how modern container-based delivery works.

### 5. `05-kubernetes`
- **Focus:** Container Orchestration.
- **Details:** Upgrades the deployment target to a Kubernetes cluster. It contains a `k8s` directory with Kubernetes manifest files. The deployment pipeline automates deploying to the cluster and includes an `acceptance-test.js` to automatically validate the deployment on Kubernetes.

### 6. `06-advanced-project`
- **Focus:** Advanced CI/CD Patterns and Code Quality.
- **Details:** Integrates modern enterprise patterns. Uses `poetry` for Python dependency management. It splits pipelines logically into `Jenkinsfile-Code-Quality` (for running comprehensive checks, linting, etc.) and `Jenkinsfile-Release` (for robust release automation and deployment).

## Course Material
- **`Jenkins_Project.pdf`**: This file contains the theoretical aspects, technical diagrams, and detailed instructions that accompany this hands-on code project.

## About the Application
The application being deployed throughout these steps is a purposefully simple Python Flask web application. Keeping the application logic simple ensures that the focus remains entirely on mastering the CI/CD toolchain infrastructure (Jenkins, Docker, Kubernetes, AWS) rather than getting bogged down in application complexities.
