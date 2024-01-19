FROM redis:7.2.3

RUN mkdir /etc/redis

RUN touch /etc/redis/redis.log
RUN chmod 660 /etc/redis/redis.log
RUN touch /etc/redis/sentinel.log
RUN chmod 660 /etc/redis/sentinel.log
RUN chown redis:redis /etc/redis

COPY ./docker/redis/slave1/redis.conf /etc/redis/redis.conf
COPY ./docker/redis/slave1/sentinel.conf /etc/redis/sentinel.conf

WORKDIR /etc/redis

CMD ["sh", "-c", "redis-server /etc/redis/redis.conf && redis-sentinel /etc/redis/sentinel.conf"]