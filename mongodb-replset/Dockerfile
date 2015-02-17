FROM dockerfile/mongodb:latest

MAINTAINER tattsun <t.t.mc1192.sf@gmail.com>

RUN mkdir -p /data/node1 && \
    mkdir -p /data/node2 && \
    mkdir -p /data/node3

ADD ./run /root/run

EXPOSE 27017 27018 27019
CMD ["/root/run"]
