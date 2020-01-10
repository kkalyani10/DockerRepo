#Docker file for apache for DockerRepo
FROM centos:7
MAINTAINER kalyani10kulkarni@gmail.com
RUN yum -y update 

#Below approach to use when we have multiple commands to RUN, hence add to script file

#ADD scripts /opt
#RUN chmod 755 /opt/*
#RUN /opt/packages

#Above three commands using scrips/packages file or following one command
RUN yum -y install httpd php php-gd php-mysql

ADD code /var/www/html
#COPY code/* /var/www/html
ENV MY_DB_HOST_WRITE=test
EXPOSE 80
CMD ["httpd", "-D", "FOREGROUND"]