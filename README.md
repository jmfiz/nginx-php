## Introduction
This is a Dockerfile to build a container image for nginx and php.

## Nginx Versions
- Mainline Version: **1.9.3**
- Stable Version: **1.8.0**
- *Latest = Mainline Version*

## Installation
Pull the image from the docker index rather than downloading the git repo. This prevents you having to build the image on every docker host.

```
docker pull jmfiz/nginx-php
```

## Running
To simply run the container:

```
sudo docker run --name nginx -p 8888:80 -d jmfiz/nginx-php
```
You can then browse to http://\<docker_host\>:8888 to view the default install files.
### Volumes
If you want to link to your web site directory on the docker host to the container run:

```
sudo docker run --name nginx -p 8888:80 -v /your_code_directory:/usr/share/nginx/html -d jmfiz/nginx-php
```