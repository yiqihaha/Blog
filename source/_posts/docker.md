---
title: docker
date: 2017-01-16 22:01:39
tags:
---
# docker

#### Run an interactive container
```
docker run -t -i ubuntu /bin/bash
```
  -t 分配一个新的终端</br>
  -i 交互连接

#### Start a daemonized Hello world

```
docker run -d ubuntu /bin/sh -c "while true; do echo hello world; sleep 1; done"

1e5535038e285177d5214659a068137486f96ee5c2e85a4ac52dc83f2ebe4147（container ID）
```
-d 后台运行

#### Creating our own images

1. You can update a container created from an image and commit the results to an image.
```
docker commit -m "Added json gem" -a "Kate Smith" 0b2616b0e5a8 ouruser/sinatra:v2
4f177bd27a9ff0f6dc2a830403925b5360bfe0b93d476f7fc3231110e7f71b1c
```
2. You can use a Dockerfile to specify instructions to create an image.
```
mkdir sinatra
cd sinatra
touch Dockerfile
docker build -t ouruser/sinatra:v2 .
```
-t flag to identify our new image as belonging to the user ouruser

#### Setting tags on an image

```
docker tag 5db5f8471261 ouruser/sinatra:devel
```
#### Remove an image from the host
```
 docker rmi training/sinatra
```
