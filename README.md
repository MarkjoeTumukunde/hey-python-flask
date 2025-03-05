# Flask Dockerized Web Application

This repository contains a simple web application built with Flask, containerized using Docker.
The app responds with a simple message: "Hello, Containerized World!" when accessed through the web browser.

## Project Overview

This project demonstrates how to containerize a basic Flask application using Docker. 
The container allows you to run the Flask app consistently across different environments without needing to worry about dependency installation on each machine.

### Technologies Used:
- **Python 3.9** - Base image for the application.
- **Flask** - Lightweight web framework for Python.
- **Docker** - Containerization platform used to package the app.

## Prerequisites

Before running the application, ensure that you have the following installed:

- [Docker](https://www.docker.com/get-started)
- [Git](https://git-scm.com/downloads)
### the process of containerizing a basic web application using Docker.
- Create the Flask web application
- Create a requirements.txt File. This is necessary to specify all the dependencies that the Flask application needs.
- Create the Dockerfile. The Dockerfile is the script that defines how the Docker image is built. It contains all the instructions needed to setup the container environemtn, install dependencies, copy the application and specify how to run it
- Build the docker image. This is achieved by running the following commands ***docker build -t imagename .***
- Run the docker container
- Access the Flask Application. Once the container is running, we can access the Flask application from a web browser at http//localhost:port eg http://localhost:5000
- Stop the Docker container. To stop the running container we press ***CTRL + C*** in the terminal where the container is running.
- Push the Docker image to the Docker Hub. This is optional but if you want to share your Docker image, you can deploy it to a cloud services like Docker Hub.
  
### Role of Kubernetes in container orchestration
**Kubernetes** is an open source platform designed to automate the development, scaling and management of containerized applications.
It acts as **a container orchestrator** that makes it easier to run large scale applications reliably by managing the lifecycle of containers.
In the case of my application, Kubernetes can be used to manage multiple instances of the dockerized flask application hence ensuring that it is always available and can handle varying levele of traffic.
- Scaling
Kubernetes allows you to easily scale the number of containers (pods) running flask application.
When traffic increases, kubernetes can automatically scale the number of replicas (containers) to meet demand hence ensuring the        application to remain responsive even under heavy load.
- Loading
Kubernetes automatically distibutes network traffic to the application containers (pods) using services which ensures that no         single container is overwhelmed with traffic hence improving performance and availability.
- Self healing.
If a container running the flask application crashes or becomes unhealthy, kubernetes automatically restarts or replaces the container to ensure that the application stays up and running.
- Rolling updates.
Kubernetes supports rolling updates which means you can deploy new versions of the flask app without downtime. It will gradually replace old versions of the containers with the new ones hence ensuring that the application remains accessible while updates are being applied.
