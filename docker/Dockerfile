FROM alpine:edge

LABEL maintainer "Justin Kulesza <justin.kulesza@atomicobject.com>"

RUN apk update && \
    apk add \
        apache2 && \
    rm -rf /var/cache/apk/*

RUN mkdir -p /var/www/localhost/htdocs

ADD . /var/www/localhost/htdocs

WORKDIR /var/www/localhost/htdocs

ENTRYPOINT ./bin/docker_entrypoint
