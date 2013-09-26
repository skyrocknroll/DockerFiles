#Ubuntu 12.04 with the basic required packages
MAINTAINER Yuvaraj L email : uvaraj6@gmail.com

# Base image
FROM ubuntu

#Add the universe sourcelist
RUN echo deb http://us.archive.ubuntu.com/ubuntu/ precise universe >> /etc/apt/sources.list

#Add internal java Repo
RUN echo deb ftp://10.30.0.42/debs/ amd64/ >> /etc/apt/sources.list

#Install install internal repo proxy
RUN wget -N http://10.30.0.42:3142/canverarepoproxy/install.sh && bash install.sh
RUN rm install.sh
RUN apt-get update
RUN apt-get install -y vim iputils-ping net-tools apt-utils dialog

ENTRYPOINT ["/bin/bash"]
