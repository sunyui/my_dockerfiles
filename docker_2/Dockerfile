FROM centos:latest
MAINTAINER Sun yan

RUN yum -y install wget
RUN wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-6.repo
RUN yum clean all
RUN yum makecache
RUN yum -y update
RUN yum install ruby ruby-devel redis

# RUN apt-get update && apt-get -y install ruby ruby-dev build-essential redis-tools
RUN gem install --no-rdoc --no-ri sinatra json redis

RUN mkdir -p /home/www/sites/webapp

EXPOSE 4567

CMD [ "/home/www/sites/webapp" ]