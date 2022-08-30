FROM centos:7

RUN yum update -y && \
# Need epel-release for some packages
yum install -y epel-release && \
# Install required packages
# cabextract xorg-x11-font-utils fontconfig for fonts
yum install -y \
    glibc.i686 \
    curl \
    cabextract \
    xorg-x11-font-utils \
    fontconfig \
    wget \
    net-tools \
    zip \
    unzip \
    p7zip \
    which \
    dos2unix
COPY msttcore-fonts-installer-2.6-1.noarch.rpm /root/msttcore-fonts-installer.rpm
WORKDIR /root
RUN rpm -i msttcore-fonts-installer.rpm && \
    rm -f msttcore-fonts-installer.rpm && \
# Install all of our other needed fonts
yum install -y liberation-fonts liberation-fonts-common liberation-mono-fonts liberation-narrow-fonts liberation-sans-fonts liberation-serif-fonts && \
yum install -y dejavu-fonts-common dejavu-sans-fonts dejavu-sans-mono-fonts dejavu-serif-fonts && \
yum install -y google-noto-sans-devanagari-fonts