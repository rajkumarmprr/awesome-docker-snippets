# Manage multiple containers


## Ask

1. Run a **nginx**, a **mysql**, and a **httpd** (apache) server
2. Run all of them **--detach** (or **-d**), name them with **--name**
3. nginx should listen on **80:80**, httpd on **8080:80**, mysql on **3306:3306**
4. When running mysql, use the **--env** option (or **-e**) to pass in **MYSQL_RANDOM_ROOT_PASSWORD=yes**
5. Use **docker container logs** on mysql to find the random password it created on startup
6. Clean it all up with **docker container stop** and **docker container rm**
7. Use **docker container ls** to ensure everything is correct before and after cleanup


## Answer

```bash
docker container run --name nginx --publish 80:80 --detach nginx
docker container run --name apache --publish 8080:80 --detach httpd
docker container run --name mysql --publish 3306:3306 --detach --env MYSQL_RANDOM_ROOT_PASSWORD=yes mysql
docker container logs -f mysql
docker container ls -a
docker stop nginx apache mysql
docker rm nginx apache mysql
docker container ls -a
```