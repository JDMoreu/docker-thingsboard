# Docker-thingsboard

## Getstart

- Install Docker and Docker-compose

```azurecli-interactive
apt install docker.io
apt install docker-compose
``` 

- Install git

```azurecli-interactive
apt install git
``` 

- Clone the repository

```azurecli-interactive
git clone https://github.com/JDMoreu/docker-thingsboard.git
cd docker-thingsboard
``` 

- Create directories for logs and data 

```azurecli-interactive
mkdir -p ~/.mytb-data && sudo chown -R 799:799 ~/.mytb-data
mkdir -p ~/.mytb-logs && sudo chown -R 799:799 ~/.mytb-logs
``` 

- Run docker-compose 

```azurecli-interactive
docker-compose pull
docker-compose up -d
docker-compose logs -f mytb
``` 
- Open ports

```azurecli-interactive
sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT
sudo iptables-save > /etc/iptables/rules.v4
``` 






