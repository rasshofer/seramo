FROM alpine
MAINTAINER SpaceMesh <hello@spacemesh.com>

RUN apk update && apk upgrade && apk add --no-cache apache2 apache2-utils

RUN rm -rf /var/cache/apk/*

RUN mkdir /web && chown -R apache:apache /web
RUN sed -i 's#^DocumentRoot ".*#DocumentRoot "/web"#g' /etc/apache2/httpd.conf
RUN sed -i 's#AllowOverride none#AllowOverride All#' /etc/apache2/httpd.conf
RUN sed -i 's/#ServerName/ServerName/' /etc/apache2/httpd.conf
RUN sed -i 's/#LoadModule\ rewrite_module/LoadModule\ rewrite_module/' /etc/apache2/httpd.conf

VOLUME /web

EXPOSE 80

CMD httpd -D FOREGROUND
