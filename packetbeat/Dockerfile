FROM docker.elastic.co/beats/packetbeat:6.4.2

COPY config/*.yml /usr/share/packetbeat/

USER root

RUN chown -R root:root /usr/share/packetbeat/
RUN chmod -R go-w /usr/share/packetbeat/
