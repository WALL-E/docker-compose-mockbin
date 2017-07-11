
FROM hub.c.163.com/library/centos:7.2.1511
COPY ENTRYPOINT.sh /ENTRYPOINT.sh
RUN ["yum", "update", "-y"]
RUN ["yum", "install", "-y", "epel-release"]
RUN ["yum", "install", "-y", "redis"]
RUN chmod +x /ENTRYPOINT.sh
COPY redis.conf /etc/redis_default.conf
EXPOSE 6379
ENTRYPOINT /ENTRYPOINT.sh

