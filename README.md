# web-application 
# A Simple Web Application Deployed with Docker and Kubernetes

## Overview
This project demonstrates how to containerize a simple web application using Docker and deploy it on a Kubernetes cluster. The web application is built using Python Flask and displays a "Hello World!" message. The project includes a Dockerfile for containerization, Kubernetes Deployment and Service files for deployment.

## Prerequisites
- Python 3.8 or higher
- Docker
- Kubernetes cluster
- kubectl command-line tool
- A Docker Hub account

## Project Structure

MyWebApp/

├── app.py # Python Flask application

├── Dockerfile # Dockerfile to build the image

├── deployment.yaml # Kubernetes Deployment file

├── service.yaml # Kubernetes Service file

└── README.md # Project documentation


## Instructions

### 1. Repository

- To Clone the repository:
  ```bash
  git clone https://github.com/YamanOnur/web-application.git
- Go to the directory:
  ```bash
  cd web-application

### 2. Creating the Docker Image

- Build the Docker image using:
  ```bash
  docker build -t web-application:latest .
- Test the docker image using:
  ```bash
  docker run -p 5000:5000 web-application:latest
The application should be accessible at http://localhost:5000.

### 3. Deploying the Application on Kubernetes

- Apply the Kubernetes Deployment file:
  ```bash
  kubectl apply -f deployment.yaml
- Apply the Kubernetes Service file:
  ```bash
  kubectl apply -f service.yaml
- Verify that the application is running:
  ```bash
  kubectl get pods
- Access the Application:
  ```bash
  kubectl get services
- Verify that the application displays "Hello World!" by accessing the external IP or domain.

### Pull the image from dockerhub
  ```bash
  docker pull onryaman/web-application

## Conclusion

This project demonstrates how to deploy a simple web application using Docker and Kubernetes. The application is scalable, easily accessible, and documented for future reference.


  
