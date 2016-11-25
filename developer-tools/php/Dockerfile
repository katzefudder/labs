FROM ubuntu:16.04

RUN apt-get update
RUN apt-get -y install apache2 libapache2-mod-php php php-mysql php-xdebug mysql-client

COPY config/xdebug.ini /etc/php/7.0/cli/conf.d/xdebug.ini
COPY config/xdebug.ini /etc/php/7.0/apache2/conf.d/xdebug.ini

WORKDIR /var/www/html

CMD ["apachectl", "-D", "FOREGROUND"]