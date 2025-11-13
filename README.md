🚀 CI/CD Pipeline with GitHub Actions, Docker & DockerHub

This repository contains a fully automated CI/CD pipeline for a simple Node.js web application.
The pipeline uses GitHub Actions to:

Build the application

Run tests

Create a Docker image

Push the image to DockerHub

This ensures your application is containerized, tested, and published automatically every time you push to the main branch.

📁 Project Structure
.
├── server.js
├── package.json
├── Dockerfile
└── .github/
    └── workflows/
        └── deploy.yml

🧠 Overview

This project demonstrates:

Continuous Integration (CI)

Continuous Delivery (CD)

Containerization using Docker

Automated DockerHub publishing

Version-controlled infrastructure using GitHub Actions

🛠 Tech Stack
Tool	Purpose
Node.js	Web application runtime
Docker	Containerization
GitHub Actions	CI/CD automation
DockerHub	Image registry
▶️ Running the App Locally
1. Install dependencies
npm install

2. Start the server
npm start

3. The server runs on:
http://localhost:3000

🐳 Build & Run with Docker
Build the Docker image
docker build -t cicd-demo-app .

Run the container
docker run -p 3000:3000 cicd-demo-app

📦 Pull the Image from DockerHub

Anyone can pull the auto-built image from DockerHub:

docker pull <your-dockerhub-username>/cicd-demo-app:latest
docker run -p 3000:3000 <your-dockerhub-username>/cicd-demo-app

🔄 CI/CD Pipeline Flow

Developer pushes code to main

GitHub Actions triggers workflow

Node.js dependencies are installed

Tests are executed

Docker image is built

DockerHub login happens via GitHub Secrets

Image is pushed to DockerHub automatically

🔐 Required GitHub Secrets

Add these in your repo:

Secret Name	Description
DOCKERHUB_USERNAME	Your DockerHub username
DOCKERHUB_TOKEN	DockerHub access token (Read/Write)
🧩 GitHub Actions Workflow

The full workflow file is located at:

.github/workflows/deploy.yml


This workflow builds, tests, packages, and publishes the application to DockerHub on every push.

🎯 Key Advantages

Zero manual deployment

Automated Docker builds

Version-controlled CI/CD setup

Faster, reliable delivery pipeline

Perfect for DevOps practice and learning
