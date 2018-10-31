FROM docker.elastic.co/logstash/logstash:6.2.3

COPY config/*.conf /usr/share/logstash/pipeline/
COPY conf.d/*.json /usr/share/logstash/conf.d/

USER root

RUN mkdir /usr/share/logstash/GeoIP

RUN curl -LO "http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz" && \
    gunzip GeoLite2-City.tar.gz && \
    find ./ -name '*GeoLite2-City*' | xargs -I '{}' mv {} /usr/share/logstash/GeoIP/GeoLite2-City.mmdb

RUN chown -R root:root /usr/share/logstash/
RUN chmod -R go-w /usr/share/logstash/