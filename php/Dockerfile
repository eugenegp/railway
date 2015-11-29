FROM php:5.6-cli

MAINTAINER Eugene Stepanov <eugeneiso@gmail.com>

# Install mbstring Extension

RUN apt-get update && apt-get -y install zlib1g-dev libsasl2-dev libssl-dev && \
    docker-php-ext-install mbstring bcmath zip && pecl install mongodb && \
    cd /usr/src/php && make clean && \
    apt-get purge -y --auto-remove zlib1g-dev libsasl2-dev libssl-dev

ADD timezone.ini /usr/local/etc/php/conf.d/timezone.ini
ADD mongodb.ini /usr/local/etc/php/conf.d/

WORKDIR /opt/app/scraper