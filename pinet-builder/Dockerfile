FROM centos:7

LABEL createdBy="huangxuantao"
LABEL goVersion="1.16"

ENV goPackage=go1.16.linux-amd64.tar.gz
ENV goUrl=https://gomirrors.org/dl/go/$goPackage

ENV upxFolder=upx-3.96-amd64_linux
ENV upxPackage=$upxFolder.tar.xz
ENV upxUrl=https://github.com/upx/upx/releases/download/v3.96/$upxPackage

WORKDIR /root/go

RUN yum install -y git make wget libnl3-devel

RUN cd /usr/local/src; wget $goUrl; tar zxvf $goPackage -C /usr/local
RUN ln -nsfv /usr/local/go/bin/* /usr/bin/
RUN mkdir -p /root/go

RUN cd /usr/local/src; wget $upxUrl; tar xvJf $upxPackage -C /usr/local
RUN ln -nsfv /usr/local/$upxFolder/upx /usr/bin/
