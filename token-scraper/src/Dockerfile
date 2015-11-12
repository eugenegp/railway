FROM pataquets/phantomjs

MAINTAINER eugeneiso

ENV TOKEN_SCRAPER_VERSION 0.1

RUN mkdir -p /opt/app

ADD token-scraper.js /opt/app/token-scraper.js

WORKDIR /opt/app

EXPOSE 8666

# Default command
CMD ["/usr/local/bin/phantomjs", "token-scraper.js", "8666"]
