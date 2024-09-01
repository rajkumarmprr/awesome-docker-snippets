# Docker commands

The docker commands and there usage

## What is docker?

Docker is a platform its allow the developer to quickly develop, ship and deploy their application.

## What is docker container

Docker container is an running instance of image as a process or we say it is an instance of running image as a process.

### What is docker image

Docker image is a application that we want to run, It contains the source codes, libraries and dependencies as a package to run the application.


## Docker command syntax

### New way
```bash
  docker <management-command> <sub-command> [options]
```
#### Example
```bash
  docker container logs <name/id>
```
### Old way
```bash
  docker <command> [options]
```
#### Example
```bash
  docker logs <name/id>
```

| Command                                                                     | Usage                                                                            |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| docker version                                                              | To check the docker client and docker engine version                             |
| docker info                                                                 | To check the docker configs information                                          |
| docker image ls / docker images                                             | To list the all available docker images in the system                           |
| docker container run / docker run                                           | To create a docker container                                                     |
| docker container ls -a / docker ps -a                                       | To list the all the containers in the system                                     |
| docker container stop <name/id> / docker stop <name/id>                     | To stop the running dokcer container using its name/id                           |
| docker container start <name/id> / docker start <name/id>                   | To start the stopped docker container and make it running                        |
| docker container rm -f <name/id> / docker rm -f <name/id>                   | To forcefully remove the docker container                                        |
| docker container top <name/id> / docker top <name/id>                       | To list the processes running in the container                                   |
| docker container logs <name/id> / docker logs <name/id>                     | To get the docker container logs                                                 |
| docker container --help                                                     | To list the all the available docker commands under the container management cmd |
| docker container run -it / docker run -it                                   | To run docker container in interactive mode                                      |
| docker container exec -it / docker exec -it                                 | To interactive the existing running docker cntainer                              |
| docker container inspect <id> / docker inspect <id>                         | To get the configs and metadata of a container                                   |
| docker container stats -a / docker stats -a                                 | To get the stats of running containers like cpu usage, memory usage and so on    |
| docker pull <image-tag>                                                     | To pull the specified docker images from the docker hub (docker image repository)|
| docker container port <name/id> / docker port <name/id>                     | To get the docker container running ports                                        |
| docker network ls                                                           | To list all the available docker virtual networks                                |
| docker network inspect <name/id>                                            | To check the specfic network configurations                                      |
| docker network create <name> --driver bridge                                | To create a new docker virtual network                                           |
| docker network connect <network-id> <contaier-id>                           | To attach the specified docker virtual network to docker container               |
| docker network disconnect <network-id> <container-id>                       | To detach the specified docker virtual network from docker container             |
