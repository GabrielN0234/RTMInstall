FROM php:7.2.10-fpm

RUN apt-get update && apt-get install -y mysql-client apt-utils
RUN docker-php-ext-install mysqli opcache && docker-php-ext-enable mysqli
RUN apt-get update -y && apt-get install -y libpng-dev

RUN apt-get update && \
    apt-get install -y \
        zlib1g-dev unzip

RUN docker-php-ext-install zip

RUN docker-php-ext-install gd

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

RUN mkdir -p /var/www
WORKDIR /var/www

