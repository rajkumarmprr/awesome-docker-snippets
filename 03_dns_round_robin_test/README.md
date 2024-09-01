# DNS Round Robin (RR) Test

> **Note:** Ever since Docker Engine 1.11, we can have multiple containers on a created network respond to the same DNS address

## Ask
1. Create a new virtual network called ***dude** (defaul bridge driver)
2. Create two containers from ***elasticsearch:2*** image
3. Research and use --network-alias search when creating them to give them an additional DNS name to respond to
4. Run ***alpine nslookup search*** with ***--net*** to see the two containers list from the same DNS name
5. Run ***centos curl -s search:9200*** with ***--net*** multiple times until you see both "name" fields show


## Answer
```bash
docker network ls
docker network create dude --driver bridge
docker container run -d --name es1 --net dude --net-alias search elasticsearch:2
docker container run -d --name es2 --net dude --net-alias search elasticsearch:2
docker container ls
docker container run --rm -it --name alpine --net dude alpine nslookup search
docker container run --rm -it --name centos --net dude centos:7 curl -s search:9200
docker container stop es1 es2
docker container rm es1 es2
docker network rm dude
```
