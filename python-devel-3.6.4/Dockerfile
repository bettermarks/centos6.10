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
  bzip2-devel

WORKDIR /usr/src
RUN wget https://www.python.org/ftp/python/3.6.4/Python-3.6.4.tgz
RUN tar xzf Python-3.6.4.tgz
WORKDIR /usr/src/Python-3.6.4
RUN ./configure --enable-optimizations
RUN make altinstall

# Replace python default bin by the python3.6
RUN rm /usr/bin/python
RUN ln -s /usr/local/bin/python3.6 /usr/local/bin/python


