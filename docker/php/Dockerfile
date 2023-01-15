FROM php:8.1.12-fpm

COPY --from=composer:2.4.4 /usr/bin/composer /usr/local/bin/composer

RUN touch /var/log/xdebug.log
RUN chmod 666 /var/log/xdebug.log

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git && \
    apt-get install zip unzip && \
    pecl install xdebug-3.1.2 && \
    docker-php-ext-enable xdebug

RUN adduser --system --no-create-home --group roman
USER roman

WORKDIR "/app"

