FROM centos:latest
MAINTAINER Sun Yan

RUN yum -y update; yum clean all
RUN yum -y install epel-release; yum clean all
RUN yum -y install redis; yum clean all

EXPOSE 6379

ENTRYPOINT ["redis-server"]

