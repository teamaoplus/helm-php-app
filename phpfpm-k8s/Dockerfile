# This Dockerfile uses the latest version of the Bitnami PHP-FPM Docker image
FROM php:7.4-fpm

# Copy app's source code to the /app directory
COPY app-code /app

# The application's directory will be the working directory
WORKDIR /app

RUN apt update && apt install -y zlib1g-dev libpng-dev && rm -rf /var/lib/apt/lists/*
RUN docker-php-ext-configure gd \
    && docker-php-ext-install gd
RUN docker-php-ext-install mysqli
