# Docker web App deployment

## Project Overview
This project demonstrates the containerization of a web application using Docker and Docker Compose. It covers creating a custom `Dockerfile`, managing a multi-container environment, configuring Docker networks, and using volumes for persistent data.

## Architecture
- **Web App:** A static HTML page served by an Nginx container (`nginx:alpine`).
- **Database:** A Redis container (`redis:alpine`) running alongside the web app.
- **Networking:** A custom bridge network (`app-network`) allowing the web app and database to communicate securely.
- **Persistent Data:** A Docker volume (`redis-data`) mounted to the Redis container to ensure data survives container restarts.

## How to Run This Project
To build the image and start the containers, run:
```bash
sudo docker compose up -d --build
```

To view the application, open your browser and go to:
**http://localhost:8080**

## Evidence & Screenshots

### 1. Terminal Build Output
![docker terminal build](https://github.com/Walcott-iam/docker-webApp-deployment/blob/main/docker%20terminal%20build.png)

### 2. Live Web Application
![Docker web page](https://github.com/Walcott-iam/docker-webApp-deployment/blob/main/docker%20web%20page%20.png)

### 3. Portainer Dashboard (Container Management)
![portainer](https://github.com/Walcott-iam/docker-webApp-deployment/blob/main/portainer.png)
