FROM docker.elastic.co/beats/metricbeat:6.4.2

COPY config/*.yml /usr/share/metricbeat/

USER root

RUN chown -R root:root /usr/share/metricbeat/
RUN chmod -R go-w /usr/share/metricbeat/