FROM docker.elastic.co/logstash/logstash:6.2.3

COPY config/*.conf /usr/share/logstash/pipeline/

RUN mkdir /usr/share/logstash/maxmind
RUN curl -LO "http://geolite.maxmind.com/download/geoip/database/GeoLiteCity.dat.gz" && \
    gunzip GeoLiteCity.dat.gz && \
    mv GeoLiteCity.dat /usr/share/logstash/maxmind

USER root