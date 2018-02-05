############################################
# Dockerfile for GeoTriples.               #
# An NKUA tool developed and maintained    #
# by the KRR&A team (http://kr.di.uoa.gr/) #
#                                          #
# GeoTriples                               #
############################################

FROM gioargyr/krratoolsbase:1.0.0

MAINTAINER Giorgos Argyriou <gioargyr@gmail.com>


# DOWNLOAD geotriples
RUN wget http://geotriples.di.uoa.gr/downloads/geotriples-1.1.6-bin.zip \
 && unzip geotriples-1.1.6-bin.zip \
 && rm -rf /geotriples-1.1.6-bin.zip
 
WORKDIR /geotriples-1.1.6-bin/bin
