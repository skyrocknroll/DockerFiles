#Ubuntu 12.04 with the basic required packages

FROM ubuntu/extended

MAINTAINER Yuvaraj L email : uvaraj6@gmail.com


RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y python-software-properties
RUN add-apt-repository ppa:rethinkdb/ppa
RUN apt-get update
RUN apt-get install -y rethinkdb
# Rethinkdb process
EXPOSE 28015
# Rethinkdb admin console
EXPOSE 8080

# Create the /rethinkdb_data dir structure
RUN /usr/bin/rethinkdb create

ENTRYPOINT ["/usr/bin/rethinkdb"]

CMD ["--help"]

