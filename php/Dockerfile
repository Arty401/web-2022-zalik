FROM php:8.0-apache

RUN apt update && apt upgrade -y \
  && apt install -y \
  g++ \
  git-core \
  curl \
  build-essential \
  openssl \
  libicu-dev \
  libpq-dev \
  libzip-dev \
  zip \
  zlib1g-dev \
  && docker-php-ext-install \
  intl \
  opcache \
  pdo \
  pdo_pgsql \
  pgsql

RUN curl -fsSL https://deb.nodesource.com/setup_current.x | bash - &&\
    apt-get install -y nodejs

WORKDIR /var/www/laravel_docker

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
