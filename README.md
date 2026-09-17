# DevOps CI/CD Pipeline using Jenkins, Docker & AWS

## 📌 Project Overview

This project demonstrates an end-to-end CI/CD pipeline for a Python Flask application using **GitHub, Jenkins, Docker, and AWS EC2**.

The pipeline automates the process of retrieving source code, building the application, running tests, creating a Docker image, and deploying the application as a Docker container on an AWS EC2 instance.

The project follows the **Pipeline as Code** approach using a Jenkinsfile.

---

## 🏗️ Architecture

```text
Developer
    │
    ▼
 GitHub Repository
    │
    ▼
   Jenkins
    │
    ├── Checkout
    ├── Build
    ├── Test
    ├── Docker Build
    └── Deploy
          │
          ▼
     Docker Container
          │
          ▼
      AWS EC2
          │
          ▼
    Flask Application
```

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| AWS EC2 | Application hosting |
| Jenkins | CI/CD automation |
| Git | Version control |
| GitHub | Source code repository |
| Docker | Application containerization |
| Python | Application development |
| Flask | Web application framework |
| Linux | Server environment |
| Shell Scripting | Pipeline automation |

---

## 🔄 CI/CD Pipeline

The Jenkins pipeline consists of the following stages:

### 1. Checkout

Jenkins retrieves the latest application source code from the GitHub repository.

### 2. Build

The application is prepared for deployment and its required dependencies are installed.

### 3. Test

The pipeline performs application testing before deployment.

### 4. Docker Build

Jenkins creates a Docker image using the project's Dockerfile.

```text
devops-app:latest
```

### 5. Deploy

The pipeline stops and removes the previous Docker container and starts a new container using the latest Docker image.

```text
devops-app-container
```

---

## 🐳 Docker

The Flask application is containerized using Docker.

### Docker Image

```text
devops-app:latest
```

### Docker Container

```text
devops-app-container
```

### Application Port

```text
5000
```

The Docker container publishes port `5000` of the application to port `5000` on the EC2 instance.

---

## ☁️ AWS Deployment

The application is deployed on an **AWS EC2 instance**.

The EC2 instance runs:

- Linux
- Jenkins
- Docker
- Flask application container

The deployed application can be accessed using:

```text
http://<EC2-PUBLIC-IP>:5000
```

---

## 📂 Project Structure

```text
devops-cicd-project/
│
├── app.py
├── Dockerfile
├── Jenkinsfile
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 📄 Jenkinsfile

The CI/CD pipeline is defined using a `Jenkinsfile`.

This follows the **Pipeline as Code** approach, allowing the pipeline configuration to be maintained along with the application source code.

### Pipeline Flow

```text
GitHub
   ↓
Checkout
   ↓
Build
   ↓
Test
   ↓
Docker
