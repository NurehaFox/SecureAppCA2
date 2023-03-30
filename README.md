SecureAppCA2
Branch: Main

# Create a Docker network
docker network create <network-name>

# Run a MySQL Docker container with a root password
docker run -d --name db -e MYSQL_ROOT_PASSWORD=my-secret-password mysql:latest

# Run the phpMyAdmin Docker container on the previously created network
docker run -d --name phpmyadmin -p <host-port>:80 --network <network-name> phpmyadmin/phpmyadmi
