FROM php:8.1-fpm

RUN apt-get update && apt-get install -y \
  git zip unzip curl libonig-dev libxml2-dev libzip-dev \
  && docker-php-ext-install pdo_mysql mbstring zip exif pcntl

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www