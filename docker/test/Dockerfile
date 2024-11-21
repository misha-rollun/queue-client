FROM php:7.1

RUN pecl install xdebug-2.9.8
RUN docker-php-ext-enable xdebug
RUN curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer

RUN apt-get update && apt-get install -y git zip

COPY ./ssh/ssh_config /etc/ssh/ssh_config

WORKDIR /data
