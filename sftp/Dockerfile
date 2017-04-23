FROM alpine:latest
MAINTAINER SpaceMesh <hello@spacemesh.com>

RUN apk update && apk upgrade && apk add --no-cache openssh openssh-sftp-server
RUN rm -rf /var/cache/apk/*

RUN mkdir -p /etc/ssh/keys

COPY sshd_config /etc/ssh/sshd_config
COPY entrypoint /entrypoint

VOLUME /etc/ssh/keys

ENTRYPOINT ["/entrypoint"]
