FROM eugenegp/phantomjs:2.0

MAINTAINER eugeneiso

ENV TOKEN_SCRAPER_VERSION 0.1

RUN mkdir -p /opt/app/token-scraper

COPY to token-scraper.js /opt/app/token-scraper

WORKDIR /opt/app/token-scraper

# Default command
CMD ["/usr/bin/phantomjs", "token-scraper.js", "8666"]
