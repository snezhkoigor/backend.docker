FROM docker.elastic.co/logstash/logstash:6.2.3

COPY config/*.conf /usr/share/logstash/pipeline/

RUN mkdir /usr/share/logstash/maxmind
RUN curl -LO "http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz" && \
    gunzip GeoLite2-City.tar.gz && \
    find ./ -name '*GeoLite2-City*' | xargs -I '{}' mv {} /usr/share/logstash/maxmind
#    mv GeoLite2-City.mmdb /usr/share/logstash/maxmind

USER root