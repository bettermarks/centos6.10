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
RUN wget https://www.python.org/ftp/python/3.6.4/Python-3.6.4.tgz
RUN tar xzf Python-3.6.4.tgz
WORKDIR /usr/src/Python-3.6.4
RUN ./configure --enable-optimizations --enable-loadable-sqlite-extensions
RUN make altinstall
