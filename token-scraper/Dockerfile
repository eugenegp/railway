FROM ubuntu:14.04

MAINTAINER eugeneiso

ENV PHANTOMJS_VERSION 2.0.0

RUN \
  apt-get update && \
  apt-get upgrade -y && \
  apt-get install -y vim wget git \
  build-essential g++ flex bison gperf ruby perl \
    libsqlite3-dev libfontconfig1-dev libicu-dev libfreetype6 libssl-dev \
    libpng-dev libjpeg-dev python libx11-dev libxext-dev && \
    cd /tmp/ && git clone git://github.com/ariya/phantomjs.git && \
    cd phantomjs && git checkout 2.0
RUN \
  cd /tmp/phantomjs && echo 'y' | ./build.sh && \
  mv /tmp/phantomjs/bin/phantomjs /usr/bin/phantomjs && \
  rm -rf /tmp/phantomjs && \
  apt-get autoremove -y && \
  apt-get clean all

# Default command
CMD ["/usr/bin/phantomjs"]
