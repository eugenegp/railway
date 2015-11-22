docker run -i -p 3000:3000 -e "GF_SERVER_ROOT_URL=http://localhost" -e "GF_SECURITY_ADMIN_PASSWORD=secret" grafana/grafana
docker run -d -p 8083:8083 -p 8086:8086 --expose 8090 --expose 8099 tutum/influxdb

Build
 
 docker build -t eugenegp/php:5.6-cli ./php
 
 docker build -t eugenegp/sales:0.1.1 ./sales
 
 docker build -t eugenegp/token:0.1.2 ./token-scraper
Run

  docker exec -it ticketspasrser_php_1 /bin/bash
