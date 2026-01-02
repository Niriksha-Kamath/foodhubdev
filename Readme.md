# 🍔 FoodHub – CI/CD Pipeline using Jenkins, Docker & Docker Compose

FoodHub is a **2-tier backend application** built with **Python Flask** and **MySQL**, integrated with a **fully automated CI/CD pipeline** using **Jenkins**.  
The project demonstrates real-world **DevOps practices** such as pipeline-as-code, containerization, automated deployments, and application–database integration — without relying on cloud-specific services.

---

## 📌 Project Overview

The objective of this project is to automate the **build and deployment process** of a backend application whenever code is pushed to GitHub.

### Key Highlights
- Automated CI/CD pipeline using **Jenkins**
- Containerized application using **Docker**
- Multi-container orchestration using **Docker Compose**
- Persistent MySQL database using Docker volumes
- Cloud-agnostic and production-ready architecture

---

## 🚀 Application Features

- Fetch food items from database
- Add new food items via REST API
- Health check endpoint
- Persistent database storage

---

## 🐳 Docker & Docker Compose

### Dockerfile
- Builds Flask application image
- Installs Python dependencies
- Exposes port `5000`

### Docker Compose
- Runs Flask and MySQL containers
- Manages container networking
- Uses volumes for MySQL data persistence

---

## 🔁 CI/CD Pipeline (Jenkins)

The Jenkins pipeline is implemented using **Pipeline-as-Code** (`Jenkinsfile`) and performs:

1. Source code checkout from GitHub
2. Docker image build
3. Application deployment using Docker Compose

Any push to the `main` branch triggers an automated deployment.

---

## 🧪 Run the Project Locally

### Prerequisites
- Docker
- Docker Compose
- Jenkins
- Git

### Steps

```bash
git clone https://github.com/Niriksha-Kamath/foodhubdev.git
cd foodhubdev
docker compose up -d --build
