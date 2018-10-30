FROM docker.elastic.co/logstash/logstash:6.2.3

COPY config/*.conf /usr/share/logstash/pipeline/

RUN mkdir /usr/share/logstash/maxmind
RUN curl -LO "http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz" && \
    gunzip GeoLite2-City.tar.gz && \
    mv GeoLite2-City.mmdb /usr/share/logstash/maxmind

USER root