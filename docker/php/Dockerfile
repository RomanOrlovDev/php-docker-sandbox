FROM php:8.1.12-fpm

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git && \
    apt-get install zip unzip

COPY --from=composer:2.4.4 /usr/bin/composer /usr/local/bin/composer

VOLUME ["/app"]
