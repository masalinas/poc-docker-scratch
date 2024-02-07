# Description
Poc Docker from scratch without any ENTRYPOINT nor CMD

## Download alpine file system 

From this url we can select one alpine file system version to be build in a image

```
https://dl-cdn.alpinelinux.org/alpine/
```

## Create Dockerfile

```
FROM scratch 
ADD alpine-minirootfs-3.11.2-x86_64.tar.gz /
COPY . /
```

## Build image 

```
docker build -t from_scratch .
Sending build context to Docker daemon  2.724MB
Step 1/3 : from scratch
-----
Successfully tagged test:1
```

## Run image 

```
docker run -ti from_scratch /bin/sh
/ #
``` 
