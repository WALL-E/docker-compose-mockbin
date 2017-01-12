
FROM hub.c.163.com/library/centos:7.2.1511
COPY ENTRYPOINT.sh /ENTRYPOINT.sh
RUN ["yum", "update", "-y"]
RUN ["yum", "install", "-y", "epel-release"]
RUN ["yum", "install", "-y", "git"]
RUN ["yum", "install", "-y", "npm"]
RUN ["git", "clone", "https://github.com/Mashape/mockbin.git", "/apps/mockbin/"]
RUN ["npm", "install", "/apps/mockbin/"]
RUN chmod +x /ENTRYPOINT.sh
COPY package.json /apps/mockbin/
COPY view.jade /apps/mockbin/src/views/bin/view.jade
EXPOSE 80
ENTRYPOINT /ENTRYPOINT.sh

