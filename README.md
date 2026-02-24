# Lab 4

## Project Demo

https://youtu.be/LmplZOkrffY



##  Project Overview

 It has Python Flask web app that communicates with  Redis database to track and count visitors on it



---

##  Reflection Questions

### 1. What is the difference between a Docker Image and a Docker Container?
A **Docker Image** is a read only template that has the application code, environment and dependencies
A **Docker Container**  running instance of an image.
it  is image as the "class" and the container as the "object"

### 2. How does Docker's use of layers improve build efficiency?
Docker builds images stages, where each instruction in a Dockerfile puts  new layer other
Docker has caching to skip rebuilding nothing changed in previous build
very less time needed for repeated builds 

### 3. What is the purpose of the writable layer in a container?

Each of the containers contains a thin writable top layer over the read-only image layers.
This layer enables it to have temporary data, logs or modified files without impacting the base image.
At the time when the container is deleted, the data on this writable layer is lost unless a volume is employed.

### 4. What are the benefits of using Docker Compose for multi-container applications?

Orchestration:  describe and control set of services through one docker-compose.yml file
Automation:  one command to start the application: docker compose up
Internal Networking: Compose will build up automatically created network in which containers can access other containers with their service names 

## Run Locally

1. Clone this repository on local.
2. `cd CST8915-Lab4-Docker`
3. Lunch App `docker compose up -d`
4. Access counter: `curl http://localhost:80`

---

**Would you like me to show you how to edit this directly on GitHub to save you from having to use the terminal again?**
