FROM docker.elastic.co/beats/filebeat:6.4.2

COPY config/ /usr/share/filebeat/

USER root

RUN chown -R root:filebeat /usr/share/filebeat/
RUN chmod -R go-w /usr/share/filebeat/

USER filebeat