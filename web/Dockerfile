FROM  centos:latest
MAINTAINER Bala
RUN yum install httpd wget httpd-devel php php-mysql php-fpm php-mssql zip unzip php-ldap  -y
RUN echo "WEB Container " > /var/www/html/index.html
VOLUME ["/var/www"]
EXPOSE 80
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]

