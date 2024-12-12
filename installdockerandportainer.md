# Installing Docker and Portainer on Raspberry Pi

Docker and Portainer are powerful tools for managing containers and applications.

---

## What is Docker?
Docker is a platform that allows developers to automate the deployment of applications inside lightweight, portable containers. Containers are isolated environments that include everything an application needs to run, making them ideal for consistent deployment across various systems.

---

## What is Portainer?
Portainer is a web-based management interface for Docker. It simplifies container management with a user-friendly interface, making it easier to deploy, monitor, and manage Docker containers without needing extensive command-line knowledge.

---

## Installation Steps

### Commands to Install Docker and Portainer
Execute the following commands sequentially to install Docker and Portainer on your Raspberry Pi:

```bash
# Install curl if not already installed
sudo apt-get install curl

# Install Docker
curl -sSL https://get.docker.com | sh

# Verify Docker installation
docker run hello-world

# Create a Docker volume for Portainer data
docker volume create portainer_data

# Run the Portainer container
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v portainer_data:/data portainer/portainer-ce
Access the Portainer Web Interface
Open a browser and navigate to:

arduino
Copier le code
https://<Your-Raspberry-Pi-IP>:9443
Follow the on-screen instructions to:

Set up an admin user.
Start managing your containers via the Portainer dashboard.
Summary
Docker provides a containerized environment for running applications.
Portainer adds a web interface for managing Docker containers.
Together, they enable efficient application deployment and management on your Raspberry Pi.
