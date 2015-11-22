FROM pataquets/phantomjs

MAINTAINER eugeneiso

ENV TOKEN_SCRAPER_VERSION 0.1.4

RUN apt-get update && apt-get install -y node npm && apt-get install -y nodejs-legacy && apt-get purge -y --auto-remove && apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && \
    mkdir -p /opt/app/

ADD https://github.com/eugenegp/token-scraper/archive/v${TOKEN_SCRAPER_VERSION}.tar.gz /tmp/
RUN mkdir -p /opt/app/token-scraper && cd /tmp && tar -xzvf v${TOKEN_SCRAPER_VERSION}.tar.gz && \
    mv /tmp/token-scraper-${TOKEN_SCRAPER_VERSION}/* /opt/app/token-scraper && \
    cd /opt/app/token-scraper && npm install

WORKDIR /opt/app/token-scraper

EXPOSE 8666

# Default command
CMD ["./start.sh"]
