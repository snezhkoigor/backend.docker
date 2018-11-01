FROM docker.elastic.co/beats/heartbeat:7.0.0-alpha1

COPY config/*.yml /usr/share/heartbeat/

USER root

RUN chown -R root:root /usr/share/heartbeat/
RUN chmod -R go-w /usr/share/heartbeat/
