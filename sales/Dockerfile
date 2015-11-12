FROM php:5.6-cli

MAINTAINER Eugene Stepanov <eugeneiso@gmail.com>

# Install mbstring Extension
RUN docker-php-ext-install mbstring bcmath && cd /usr/src/php && make clean

WORKDIR /opt/app/scraper