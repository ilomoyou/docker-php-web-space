ARG REDIS_VERSION
ARG REDIS_HOST_PORT

FROM ${REDIS_VERSION}

EXPOSE ${REDIS_HOST_PORT}

LABEL maintainer="lsj_moon@163.com"

# 配置 redis.conf
COPY ./conf/redis.conf /usr/local/etc/redis/redis.conf

# 创建 redis.log
RUN mkdir /logs \
    && touch /logs/redis.log

# 运行 redis
CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]
