FROM centos:latest
MAINTAINER Sun Yan

RUN yum -y update; yum clean all
RUN yum -y install epel-release; yum clean all
RUN yum -y install nodejs; yum clean all
RUN yum -y install npm; yum clean all
RUN npm install -g n; n stable

EXPOSE 80

ENTRYPOINT ["node"]
CMD ["-v"]
