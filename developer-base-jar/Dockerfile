FROM itechpros/openjdk:8
ARG SERVOY_VERSION_MAJOR
ARG SERVOY_VERSION_BUILD
ENV SERVOY_VERSION_MAJOR=${SERVOY_VERSION_MAJOR}
ENV SERVOY_VERSION_BUILD=${SERVOY_VERSION_BUILD}
RUN mkdir -p /usr/home/servoy
WORKDIR /usr/home/servoy
# Install Servoy
COPY servoy_install.xml /usr/home/servoy/servoy_install.xml
RUN wget --output-document servoy_installer.jar "http://servoyguy.com/docker/download/servoy.php?version=${SERVOY_VERSION_MAJOR}&build=${SERVOY_VERSION_BUILD}&type=jar" && \
    java -jar servoy_installer.jar servoy_install.xml
