FROM centos:centos6.10

LABEL maintainer="bettermarks"

RUN yum -y install \
  scl-utils \
  centos-release-scl-rh \
  wget \
  curl \
  gcc \
  gcc-c++ \
  openssl-devel \
  bzip2-devel \
  sqlite-devel

WORKDIR /usr/src
RUN wget https://www.python.org/ftp/python/3.6.8/Python-3.6.8.tgz
RUN tar xzf Python-3.6.8.tgz
WORKDIR /usr/src/Python-3.6.8
RUN ./configure --enable-optimizations --enable-loadable-sqlite-extensions
RUN make altinstall
