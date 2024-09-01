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
### Old way
```bash
  docker <command> [options]
```


| #Command                                                                    | #Usage                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| docker version                                                              | To check the docker client and docker engine version                             |
| docker info                                                                 | To check the docker configs information                                          |
| docker images                                                               | To list the all available docker images in the system                            |
| docker container run / docker run                                           | To create a docker container                                                     |
| docker container ls -a / docker ps -a                                       | To list the all the containers in the system                                     |
| docker container stop <name/id> / docker stop <name/id>                     | To stop the running dokcer container using its name/id                           |
| docker container start <name/id> / docker start <name/id>                   | To start the stopped docker container and make it running                        |
| docker container rm -f <name/id> / docker rm -f <name/id>                   | To forcefully remove the docker container
| docker container top <name/id> / docker top <name/id>                       | To list the processes running in the container                                   |
| docker container logs <name/id> / docker logs <name/id>                     | To get the docker container logs                                                 |
| docker container --help                                                     | To list the all the available docker commands under the container management cmd |