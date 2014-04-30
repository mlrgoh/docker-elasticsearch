FROM ubuntu:12.04
MAINTAINER Richard Goh <mukling@gmail.com>

RUN apt-get -y update
RUN apt-get -y install wget
RUN apt-get -y install openjdk-7-jdk
RUN wget -O - http://packages.elasticsearch.org/GPG-KEY-elasticsearch | apt-key add -
RUN echo "deb http://packages.elasticsearch.org/elasticsearch/1.1/debian stable main" >> /etc/apt/sources.list
RUN apt-get -y update
RUN apt-get -y install elasticsearch

EXPOSE 9200