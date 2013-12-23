#Ubuntu 12.04 with the basic required packages

FROM ubuntu

MAINTAINER Yuvaraj L email : uvaraj6@gmail.com


RUN apt-get install -y python-software-properties
RUN add-apt-repository -y ppa:chris-lea/redis-server
RUN apt-get update
RUN apt-get install -y redis-server
EXPOSE 6379

ENTRYPOINT ["/usr/bin/redis-server"]