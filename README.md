# **Nextcloud and NGINX Proxy Manager with Separate MariaDB Instances**


This repository contains a docker-compose.yml file and an .env file for deploying Nextcloud and NGINX Proxy Manager with isolated MariaDB instances for better performance and security.

Features
Nextcloud: Open-source file sharing and collaboration platform.
NGINX Proxy Manager (NPM): User-friendly reverse proxy with SSL management.
Isolated MariaDB Instances: Separate database containers for Nextcloud and NPM for better resource management.
Prerequisites
Docker and Docker Compose installed on your system.
Install Docker
Install Docker Compose
A domain name pointing to your server (required for NGINX Proxy Manager).
Open ports: 80, 443, and 8080.
Setup
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
2. Configure the .env File
Edit the .env file to set your custom values for database credentials, ports, and more:

dotenv
Copy
Edit
# Nextcloud MariaDB Configuration
NEXTCLOUD_DB_HOST=nextcloud-db
NEXTCLOUD_DB_PORT=3306
NEXTCLOUD_DB_NAME=nextcloud
NEXTCLOUD_DB_USER=nextcloud_user
NEXTCLOUD_DB_PASSWORD=nextcloud_password
NEXTCLOUD_PORT=8080

# NPM MariaDB Configuration
NPM_DB_HOST=npm-db
NPM_DB_PORT=3306
NPM_DB_NAME=npm
NPM_DB_USER=npm_user
NPM_DB_PASSWORD=npm_password

# NPM Ports
NPM_HTTP_PORT=80
NPM_HTTPS_PORT=443
NPM_UI_PORT=81
Replace nextcloud_password and npm_password with secure values.

3. Deploy the Stack
Start the services using Docker Compose:

Contributing
Feel free to fork the repository and submit pull requests for improvements or additional features.

License
This project is licensed under the MIT License.
