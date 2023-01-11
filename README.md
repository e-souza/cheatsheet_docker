# cheatsheet_docker
Useful Docker/Podman Commands

## List containers, images and processes
```sh
docker container ls
docker container ps
docker image ls
```

## Manage containers
```sh
sudo docker container start ID/NAME
sudo docker container stop ID/NAME
sudo docker container rm ID/NAME
```
## Run Linux instances
```sh
sudo docker container run --detach --name ID/NAME -ti -p PORT:PORT debian:latest

#Ex.:
sudo docker container run --detach --name ubuntu -ti -p 80:80 ubuntu:latest
sudo docker container run --detach --name ubuntu -e LANG=pt_BR.UTF-8 -ti -p 80:80 ubuntu:latest
```

## Get a container root shell 
```sh
sudo docker exec -u 0 -ti ID/NAME bash
```
