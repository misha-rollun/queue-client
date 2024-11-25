FROM php:8.1

RUN pecl install xdebug-3.3.2
RUN docker-php-ext-enable xdebug
RUN curl -sS https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer

RUN apt-get update && apt-get install -y git zip

COPY ./ssh/ssh_config /etc/ssh/ssh_config

COPY ./conf.d  /usr/local/etc/php/conf.d

WORKDIR /data
