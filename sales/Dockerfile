FROM eugenegp/php:5.6-cli

ENV RAILWAY_SALES_VERSION 0.1.2

MAINTAINER Eugene Stepanov <eugeneiso@gmail.com>

ADD https://github.com/eugenegp/uzticketstat/archive/v${RAILWAY_SALES_VERSION}.tar.gz /tmp/
RUN cd /tmp && tar -xzvf v${RAILWAY_SALES_VERSION}.tar.gz && \
    mv /tmp/uzticketstat-${RAILWAY_SALES_VERSION}/* /opt/app/scraper && \
    curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/bin/composer && \
    cd /opt/app/scraper && ls && \
    composer install --no-ansi --no-dev --no-interaction --no-progress --no-scripts --optimize-autoloader && \
    rm -rf /tmp/*
ADD timezone.ini /usr/local/etc/php/conf.d/timezone.ini

WORKDIR /opt/app/scraper

# Default command
CMD ["php", "/opt/app/scraper/console", "sales:start"]
