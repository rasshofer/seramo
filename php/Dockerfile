FROM seramo/apache
MAINTAINER Seramo <hello@seramo.com>

RUN apk update && apk upgrade && apk add --no-cache libressl curl openssl php7 php7-apache2 php7-openssl php7-mbstring php7-apcu php7-intl php7-mcrypt php7-json php7-gd php7-curl php7-fpm php7-mysqlnd php7-pgsql php7-sqlite3 php7-phar
RUN rm -rf /var/cache/apk/*

RUN ln -s /usr/bin/php7 /usr/bin/php

RUN cd /tmp && curl -sS https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer
