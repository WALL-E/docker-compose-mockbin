
FROM hub.c.163.com/library/centos:7.2.1511
COPY ENTRYPOINT.sh /ENTRYPOINT.sh
RUN ["yum", "update", "-y"]
RUN ["yum", "install", "-y", "epel-release"]
RUN ["yum", "install", "-y", "git"]
RUN ["yum", "install", "-y", "npm"]
RUN ["git", "clone", "https://github.com/Mashape/apiembed.git", "/apps/apiembed/"]
RUN ["npm", "install", "/apps/apiembed/"]
RUN chmod +x /ENTRYPOINT.sh
EXPOSE 8080
ENTRYPOINT /ENTRYPOINT.sh

