FROM docker.elastic.co/elasticsearch/elasticsearch:6.2.3

USER root

RUN sysctl -w vm.max_map_count=262144

EXPOSE 9200 9300
