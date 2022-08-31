ARG SERVOY_VERSION_MAJOR
ARG SERVOY_VERSION_BUILD
FROM ghcr.io/itechpros/centos:7
RUN mkdir -p /usr/home/servoy
WORKDIR /usr/home/servoy
RUN wget -O servoy_developer.tar.gz http://servoyguy.com/docker/download/servoy.php?version=${SERVOY_VERSION_MAJOR}&build=${SERVOY_VERSION_BUILD}&type=tar.gz
