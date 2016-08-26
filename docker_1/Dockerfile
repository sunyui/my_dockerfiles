# Docker for sample web
FROM centos:latest
MAINTAINER Sun Yan
RUN yum -y install wget
RUN wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-6.repo
RUN yum clean all
RUN yum makecache
RUN yum -y update
RUN wget http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm
RUN rpm -ivh nginx-release-centos-7-0.el7.ngx.noarch.rpm
RUN yum install -y nginx
ADD nginx/global.conf /etc/nginx/conf.d/
ADD nginx/nginx.conf /etc/nginx/nginx.conf
RUN mkdir -p /home/www/sites/website
EXPOSE 80