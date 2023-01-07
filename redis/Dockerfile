FROM redis:6.2.6

EXPOSE 6379

LABEL maintainer="lsj_moon@163.com"

# 配置 redis.conf
COPY ./conf/redis.conf /usr/local/etc/redis/redis.conf

# 创建 redis.log
RUN mkdir /logs \
    && touch /logs/redis.log

# 运行 redis
CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]
