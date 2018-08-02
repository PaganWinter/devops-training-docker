FROM centos:latest
MAINTAINER test@test.com
RUN yum -y install httpd
ADD code /var/www/html
EXPOSE 80
ENV applb=test
CMD ["apachectl", "-D", "FOREGROUND"]
