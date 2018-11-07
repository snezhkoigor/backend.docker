FROM bitnami/redis:latest

LABEL maintainer="Mahmoud Zalt <mahmoud@zalt.me>"

USER root

## For security settings uncomment, make the dir, copy conf, and also start with the conf, to use it
# USER root
# RUN mkdir -p /usr/local/etc/redis
# COPY redis.conf /usr/local/etc/redis/redis.conf

VOLUME /data

EXPOSE 6379

# CMD ["redis-server", "/usr/local/etc/redis/redis.conf"]
# CMD ["redis-server"]
