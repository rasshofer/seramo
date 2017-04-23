FROM httpd:alpine
MAINTAINER SpaceMesh <hello@spacemesh.com>

RUN mkdir /web && chown -R www-data:www-data /web
RUN mkdir /logs && chown -R www-data:www-data /logs

COPY spacemesh.conf /usr/local/apache2/conf/spacemesh.conf

RUN echo "Include conf/spacemesh.conf" >> /usr/local/apache2/conf/httpd.conf

VOLUME /web
VOLUME /logs
