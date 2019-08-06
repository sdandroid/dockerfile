FROM php:5.6-fpm
RUN docker-php-ext-install pdo pdo_mysql && apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng12-dev \
EXPOSE  9000
