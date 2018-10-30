FROM docker.elastic.co/logstash/logstash:6.2.3

COPY config/*.conf /usr/share/logstash/pipeline/

USER root

RUN chown -R root:root /usr/share/logstash/
RUN chmod -R go-w /usr/share/logstash/

RUN curl -LO "http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.mmdb.gz" && \
    gunzip GeoLite2-City.mmdb.gz && \
    mv GeoLite2-City.mmdb /usr/share/logstash/maxmind/GeoLite2-City.mmdb