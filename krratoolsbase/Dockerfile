#################################
# Dockerfile for base image     #
#  for KRR&A team's tools.      #
# KRR&A team                    #
# Madgik                        #
# DI @                          #
# National and Kapodistrian UoA #
#                               #
# java7                         #
# maven 3.0.5                   #
# git 1.9.1                     #
# tomcat 8.0.23                 #
#################################

FROM ubuntu:14.04

MAINTAINER Giorgos Argyriou <gioargyr@gmail.com>

ENV PORT 8080
ENV TOMCAT_MAJOR_VERSION 8
ENV TOMCAT_MINOR_VERSION 8.0.23


# INSTALL PREREQUISITIES
RUN apt-get update \
 && apt-get install -y \
    wget \
    default-jdk \
    python-apsw \
    curl \
    git \
    mercurial \
    maven \
    vim \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*


# INSTALL TOMCAT
RUN wget -q https://archive.apache.org/dist/tomcat/tomcat-${TOMCAT_MAJOR_VERSION}/v${TOMCAT_MINOR_VERSION}/bin/apache-tomcat-${TOMCAT_MINOR_VERSION}.tar.gz \
 && wget -qO- https://archive.apache.org/dist/tomcat/tomcat-${TOMCAT_MAJOR_VERSION}/v${TOMCAT_MINOR_VERSION}/bin/apache-tomcat-${TOMCAT_MINOR_VERSION}.tar.gz.md5 | md5sum -c - \
 && tar zxf apache-tomcat-*.tar.gz \
 && rm apache-tomcat-*.tar.gz \
 && mv apache-tomcat* tomcat


ADD runtomcat.sh /usr/local/bin/

RUN chmod +x /usr/local/bin/runtomcat.sh

EXPOSE $PORT

CMD ["/bin/bash", "runtomcat.sh"]
