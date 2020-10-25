FROM centos:7

LABEL createdBy="huangxuantao"
LABEL goVersion="1.14.10"

WORKDIR /root/go

RUN yum install -y git make wget libnl3-devel

RUN cd /usr/local/src; wget https://gomirrors.org/dl/go/go1.14.10.linux-amd64.tar.gz; tar zxvf go1.14.10.linux-amd64.tar.gz -C /usr/local
RUN ln -nsfv /usr/local/go/bin/* /usr/bin/
RUN mkdir -p /root/go

RUN cd /usr/local/src; wget https://github.com/upx/upx/releases/download/v3.96/upx-3.96-amd64_linux.tar.xz; tar xvJf upx-3.96-amd64_linux.tar.xz -C /usr/local
RUN ln -nsfv /usr/local/upx-3.96-amd64_linux/upx /usr/bin/
