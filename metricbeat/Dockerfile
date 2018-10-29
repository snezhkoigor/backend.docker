FROM docker.elastic.co/beats/metricbeat:6.4.2

USER root

RUN chown root:metricbeat /usr/share/metricbeat/metricbeat.yml
RUN chmod go-w /usr/share/metricbeat/metricbeat.yml

USER metricbeat