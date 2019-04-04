# docker-krrasuite
Dockerfiles for all docker-images included in the National and Kapodistrian UoA's KRR&amp;A team's tools suite.

# KRRA-SUITE
This KRRA-suite docker packs all the linked data tools developed by the [KRR&A team](http://kr.di.uoa.gr/) of the [National and Kapodistrian Univeristy of Athens](http://www.di.uoa.gr/). The KRRA-suite contains the following open source tools:
* __[Strabon](http://strabon.di.uoa.gr/).__ Strabon is a spatiotemporal RDF store. You can use it to store linked geospatial data that changes over time and pose queries using two popular extensions of SPARQL (GeoSPARQL and stSPARQL). Strabon has been shown experimentally to be the most efficient spatiotemporal RDF store available today.
* __[GeoTriples](http://geotriples.di.uoa.gr/).__ GeoTriples is a tool for transforming geospatial data from their original formats (e.g., shapefiles or spatially-enabled relational databases) into RDF.
* __[Sextant](http://sextant.di.uoa.gr/).__ Sextant is a web based and mobile ready platform for visualizing, exploring and interacting with linked geospatial data. The core feature of Sextant is the ability to create thematic maps by combining geospatial and temporal information that exists in a number of heterogeneous data sources.

You need to install docker engine for following any of the instructions below (https://www.docker.com/get-started).

## Create docker-container from docker-image:
* You can either build the docker-images from scratch (see at the end of this document) or [RECOMMENDED] use directly the pre-built docker-images that are stored in DockerHub (https://hub.docker.com/). You don't have to have an account in DockerHub. Just run the commands below (`$ docker run`). Each docker-image will be ~~downloaded~~ pulled automatically in your local machine and a docker-container will be created. 
* The general command for creating a docker-container is (terminal of your machine): `[sudo] docker run --name docker-container-name docker-image-name`
* flag `-v` can be used for mounting a directory of your host machine to the container. e.g. `-v /<some_local_dir>:/inout` Now the container dir `/inout` will see whatever you store in `/<some_local_dir>`.
* flag `-p` can be used for mapping a port from the docker-container to a port in the local machine. e.g. `-p 9090:8080` and everything that is visible in container's 8080 port, will be also visible in your host machine's 9090 port.

## Using the docker-container:
* Use (the command line of) the container (terminal of your machine): `[sudo] docker exec -it docker-container-name /bin/bash`

## General docker tips:
* Listing all docker containers (terminal of your machine): `[sudo] docker ps -a` 
* Listing docker images (terminal of your machine): `[sudo] docker images`

For more detailed information on docker, visit the [official Docker Documentation](https://docs.docker.com/).


## Build docker-images from scratch
Also, you can always build all these docker-images from scratch by running this command while you are in a directory containing the corresponding Dockerfile (each tool has a Dockerfile)
`[sudo] docker build -t docker-image-name .` 
(Attention to the dot at the end of the command.)
But, if you just want to use the tools there is no reason for such overhead. Pre-built 
