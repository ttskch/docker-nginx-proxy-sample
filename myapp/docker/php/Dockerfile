FROM php:7-fpm

RUN apt-get update \
    && apt-get install -y libicu-dev libmcrypt-dev libxml2-dev \
    && docker-php-ext-install -j$(nproc) intl mcrypt xml mbstring opcache \
    && mkdir -p /var/www

COPY php.ini /usr/local/etc/php/

WORKDIR /var/www
