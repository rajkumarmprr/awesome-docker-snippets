# CLI - App Testing

## Ask

1. Use different Linux distro containers to check ***curl*** CLI tool version
2. Use two different terminal windows to start bash in both ***centos:7*** and ***ubuntu:24.04***, using ***-it***
3. Learn the ***docker container --rm*** option so you can save cleanup
4. Ensure ***curl*** is installed and on latest version for that distro
  * ubuntu : `apt-get update && apt-get install curl`
  * centos: `yum update curl`
5. Check ***curl --version*** in linux and centos distro


## Answer

```bash
docker container run --rm --name ubuntuos -it ubuntu:24.04 bash
curl --version
apt-get update && apt-get install curl
curl --version
docker container run --rm --name centos -it centos:7 bash
curl --version
yum update curl
curl --version
```