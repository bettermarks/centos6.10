FROM centos:centos6.10

LABEL maintainer="bettermarks"
 
RUN yum install -y wget openssl sed initscripts

RUN wget http://nginx.org/packages/centos/6/x86_64/RPMS/nginx-1.14.0-1.el6.ngx.x86_64.rpm

RUN rpm -iv nginx-1.14.0-1.el6.ngx.x86_64.rpm

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
