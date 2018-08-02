# devops-training

https://drive.google.com/drive/folders/1zGjwkaR0nr9iqJcot7XBOyspzCf6VwP3

- Create VPC
- Create Internet Gateway and associate to VPC
- Create Subnets (in different Availablbilily Zones) and associate to VPC
- Create Route Table and associate to both Subnets
- Create ACL and associate to both Subnets
- Create a Load Balancer Security Group (allow 80 incoming, 80,443 outgoing)
- Create a Instances Security Group (allow above LBSG and 22 incoming)
- On EC2, create a Load Balancer, add both Subnets, assign above LBSG

- Create AMI from existing VM
- Create Launch Configuration
- Create Auto Scaling Group with above LC

## Docker Commands:

docker
```
- info : 
- ps : list running containers
- ps -a : list all containers
- run : run a container
- stop <cid|name> : stop a container
- start <cid|name> : start a container
- restart <cid|name> : restart a container
- pause <cid|name> : pause a container
- unpause <cid|name> : unpause a container
- exec : issue command inside running container
- inspect <cid|name> : view container details
- rm <cid|name> : remove a container
- images : list all images
- build : build an image
- tag : name an image
- pull : pull image from hub to local
- rmi <> : push image to hub from local
- inspect <cid|name> : info about the container

- docker run

docker run -dit --name my-apache-app -p 9000:80 -v /home/ec2-user/environment/webapp:/usr/local/apache2/htdocs/ httpd:2.4
docker run -dit --name myapache-cont -p 9000:80 -v /home/ec2-user/environment/testapp/frontend/code:/usr/local/apache2/htdocs/ myapache:1.0
```

## Dockerfile:
```
FROM
MAINTAINER
RUN
ADD
COPY
EXPOSE 80
ENV myenvvar=test
CMD ["<command>", "<arg1>", "<arg2>"]


docker build -t <img-name>:<tag> .
```
docker rm my-nginx-php
docker build -t nginx-php:1.0 .
docker run -d --name my-nginx-php -p 9000:80 nginx-php:1.0

docker run -d --name my-nginx-php -p 9000:80 nginx-php:1.0

docker exec -it my-apache-app /bin/bash
