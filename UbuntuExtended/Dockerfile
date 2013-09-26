#Ubuntu 12.04 with the basic required packages

FROM ubuntu

MAINTAINER Yuvaraj L email : uvaraj6@gmail.com

#Add the universe sourcelist
RUN echo deb http://us.archive.ubuntu.com/ubuntu/ precise universe >> /etc/apt/sources.list

#Add internal java Repo
RUN echo deb ftp://10.30.0.42/debs/ amd64/ >> /etc/apt/sources.list
RUN echo "Acquire::http { Proxy "http://10.30.0.42:3142"; };" > /etc/apt/apt.conf.d/01proxy
#Install install internal repo proxy
RUN rm install.sh
RUN apt-get update
RUN apt-get install -y vim iputils-ping net-tools apt-utils dialog

ENTRYPOINT ["/bin/bash"]
