
# This version is updated on November 2022

## Generally freezing your dependencies version isn't a great idea. But due to uncontinued developers support, this project was broken due to all the deprecated stuff. This project has old dependencies version wich may lead to security issues, Please use with cotion.


## Requirements

* Docker 18.06.0+: https://docs.docker.com/install/
* Docker Compose 3+ (on Linux): https://docs.docker.com/compose/install/
    * Docker Desktop for Mac and Windows are already bundled with Docker Compose.
    

## Installation

Ensure that you have Docker and Docker Compose installed.

Ensure that ports 6379 (Redis), 5432 (PostgreSQL), 5000 (Docker Registry), and 8080 (WALKOFF UI) are available, 
or configuration will be needed.

```
# Clone this repo & branch:
git clone -b 1.0.0-alpha.1 https://github.com/nsacyber/WALKOFF.git

# Navigate to where the docker-compose.yml is:
cd WALKOFF

# Walkoff 1.0 makes use of Docker Swarm - initialize one now:
docker swarm init

# Build and launch the docker-compose (this will take a while):
docker-compose up -d --build

# Follow logs for services (append service names from the docker-compose.yml to follow specific services):
docker-compose logs -f api_gateway

# UI is viewable at http://localhost:8080 with admin:admin as credentials
```
