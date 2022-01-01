FROM php:7.2-fpm

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    git \
    curl \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    zlib1g-dev \
    libzip-dev \
    zip \
    unzip

RUN apt-get clean && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-install gd pdo_mysql mbstring exif pcntl bcmath zip intl

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN groupadd -g 1000 www
RUN useradd -u 1000 -ms /bin/bash -g www www

RUN mkdir -p /home/$user/.composer && \
    chown -R www:www /home/$user

WORKDIR /var/www/html

USER www
