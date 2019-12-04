FROM php:fpm
# install system dependencies
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    libmcrypt-dev \
    default-mysql-client \
    libmagickwand-dev \
    openssl \
    zip unzip \
    git
# install php dependencies
RUN pecl install imagick \
    && docker-php-ext-enable imagick \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install gd
    