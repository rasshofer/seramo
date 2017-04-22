FROM httpd:alpine
MAINTAINER SpaceMesh <hello@spacemesh.com>

RUN mkdir /web && chown -R www-data:www-data /web

COPY default /etc/apache2/sites-available/default

VOLUME /web
