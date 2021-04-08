FROM centos:7

LABEL createdBy="huangxuantao"
LABEL nodeVersion="v10.13.0"

ENV nodeVersion="v10.13.0"
ENV nodeFolder=node-$nodeVersion-linux-x64
ENV nodePackage=$nodeFolder.tar.gz
ENV nodeUrl=https://nodejs.org/dist/$nodeVersion/$nodePackage

WORKDIR /root/go

RUN yum install -y git make wget libnl3-devel

RUN cd /usr/local/src; wget $nodeUrl; tar zxvf $nodePackage -C /usr/local
RUN ln -nsfv /usr/local/$nodeFolder/bin/* /usr/bin/

