# DevOps CI/CD Pipeline using Jenkins, Docker & AWS

## 📌 Project Overview

This project demonstrates a basic CI/CD pipeline for a Python Flask application using GitHub, Jenkins, Docker, and AWS EC2.

The pipeline automates the process of fetching source code, building the application, running tests, creating a Docker image, and deploying the application as a Docker container on an AWS EC2 instance.

## 🏗️ Architecture

GitHub → Jenkins → Docker Build → Docker Container → AWS EC2 → Flask Application

## 🛠️ Technologies Used

- AWS EC2
- Jenkins
- Git
- GitHub
- Docker
- Python
- Flask
- Linux
- Shell Scripting

## 🔄 CI/CD Pipeline

The Jenkins pipeline contains the following stages:

1. **Checkout** – Fetches the latest source code from GitHub.
2. **Build** – Builds the application.
3. **Test** – Performs application testing.
4. **Docker Build** – Creates the Docker image.
5. **Deploy** – Stops the previous container and deploys a new container using the latest image.

## 🐳 Docker

The Flask application is containerized using Docker.

Docker image:

```text
devops-app:latest
