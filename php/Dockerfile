FROM php:5.6-cli

MAINTAINER Eugene Stepanov <eugeneiso@gmail.com>

# Install mbstring Extension

RUN apt-get update && apt-get install zlib1g-dev && \
    docker-php-ext-install mbstring bcmath zip && cd /usr/src/php && make clean && \
    apt-get purge -y --auto-remove zlib1g-dev

ADD timezone.ini /usr/local/etc/php/conf.d/timezone.ini

WORKDIR /opt/app/scraper