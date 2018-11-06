FROM docker.elastic.co/beats/heartbeat:6.4.2

COPY config/*.yml /usr/share/heartbeat/

USER root

RUN chown -R root:root /usr/share/heartbeat/
RUN chmod -R go-w /usr/share/heartbeat/
