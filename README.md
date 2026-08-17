# DevOps Docker Task

## Student Information
**Name:** IZMAHN NASIR

**Student ID:** JUW 34677

**Course:** DevOps Principles and Practices

## Application Description
This application is a simple Node.js web application developed as part of the DevOps Principles and Practices course.

The application displays student information and demonstrates a web application running inside a Docker container.

The application is containerized using Docker, the Docker image is published to Docker Hub, and the source code is maintained in a GitHub repository.

## Technologies Used
- Git
- GitHub
- Docker
- Docker Hub
- Node.js

## Dockerfile Explanation
### FROM node:20-alpine

Uses the Node.js 20 Alpine Linux image as the base image for the application.

### WORKDIR /app

Sets `/app` as the working directory inside the Docker container.

### COPY package*.json ./

Copies the package.json and package-lock.json files into the container.

### RUN npm install

Installs the Node.js dependencies required by the application.

### COPY . .

Copies the application source files into the Docker container.

### EXPOSE 3000

Documents that the application uses port 3000.

### CMD ["npm", "start"]

Starts the Node.js application when the container is launched.

## Docker Commands

### Build the Docker Image
```bash
docker build -t devops-task:v1 .
```

### Run the Container
```bash
docker run -d -p 3000:3000 --name devops-task devops-task:v1
```

### Check Running Containers
```bash
docker ps
```

### View Container Logs
```bash
docker logs devops-task
```

### Inspect the Container
```bash
docker inspect devops-task
```

### Tag the Image
```bash
docker tag devops-task:v1 izmahnasir/devops-task:v1
```

### Login to Docker Hub
```bash
docker login
```

### Push the Image to Docker Hub
```bash
docker push izmahnasir/devops-task:v1
```

### Pull the Image from Docker Hub
```bash
docker pull izmahnasir/devops-task:v1
```

### Run the Image from Docker Hub
```bash
docker run -d -p 3000:3000 --name devops-task izmahnasir/devops-task:v1
```

## Docker Hub
Docker Hub Repository: https://hub.docker.com/r/izmahnasir/devops-task

## How to Run
The application can be run using the Docker image available on Docker Hub.

### Step 1: Pull the Docker Image
First, download the Docker image from Docker Hub:
```bash
docker pull izmahnasir/devops-task:v1
```
### Step 2: Run the Docker Container
Create and start a container using the downloaded Docker image:
```bash
docker run -d -p 3000:3000 --name devops-task izmahnasir/devops-task:v1
```
### Step 3: Check the Running Container
Verify that the Docker container is running successfully:
```bash
docker ps
```
### Step 4: Open the Application in Browser
Open a web browser and go to:
```bash
http://localhost:3000
```
The application will be displayed in the browser.

## Screenshots

<img src="images/Screenshot 1.png" width="700">

<img src="images/Screenshot 2.png" width="700">

<img src="images/Screenshot 3.png" width="700">

<img src="images/Screenshot 4.png" width="700">

<img src="images/Screenshot 5.png" width="700">

<img src="images/Screenshot 6.png" width="700">

<img src="images/Screenshot 7.png" width="700">

<img src="images/Screenshot 8.png" width="700">

## Submission Links

GitHub Repository: https://github.com/izmahnasir20/devops-docker-task

Docker Hub Repository: https://hub.docker.com/r/izmahnasir/devops-task
