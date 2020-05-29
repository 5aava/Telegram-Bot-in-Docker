FROM php:7.2-fpm

RUN apt-get update
RUN apt-get install -y curl

RUN apt-get install -y libzip-dev zip \
  && docker-php-ext-configure zip --with-libzip \
  && docker-php-ext-install zip

RUN docker-php-ext-install mysqli pdo pdo_mysql

RUN curl -s https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer