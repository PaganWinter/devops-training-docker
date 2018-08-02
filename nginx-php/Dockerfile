FROM ubuntu:latest
MAINTAINER test@test.com

RUN apt-get -y update

ENV TZ=Asia/Kolkata
RUN apt-get -y install tzdata

ADD config /opt
RUN apt-get -y install `cat /opt/packages`

ADD code /var/www/html

EXPOSE 80

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]

#docker rm my-nginx-php
#docker build -t nginx-php:1.0 .
#docker run -dit --name my-nginx-php -p 9000:80 nginx-php:1.0
