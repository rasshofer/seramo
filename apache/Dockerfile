FROM httpd:alpine
MAINTAINER SpaceMesh <hello@spacemesh.com>

RUN mkdir /web && chown -R www-data:www-data /web

COPY spacemesh /etc/apache2/conf.d/spacemesh

VOLUME /web
