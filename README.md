# Docker-thingsboard

## Install dependencies

```azurecli-interactive
apt install docker.io docker-compose git
``` 

## Clone the repository

```azurecli-interactive
git clone https://github.com/JDMoreu/docker-thingsboard.git
cd docker-thingsboard
``` 

## Create directories for logs and data 

```azurecli-interactive
mkdir -p ~/.mytb-data && sudo chown -R 799:799 ~/.mytb-data
mkdir -p ~/.mytb-logs && sudo chown -R 799:799 ~/.mytb-logs
``` 

## Run docker-compose 

- Mount the config of docker-compose.yml

```azurecli-interactive
docker-compose pull
``` 

- Upload container

```azurecli-interactive
docker-compose up -d
```
- Listening mode

```azurecli-interactive
docker-compose logs -f mytb
```

## Open ports

- Opening the ports depends on the distribution you are using or if you are using a VPS or cloud server.

## User login

- System Administrator: sysadmin@thingsboard.org / sysadmin
- Tenant Administrator: tenant@thingsboard.org / tenant
- Customer User: customer@thingsboard.org / customer






