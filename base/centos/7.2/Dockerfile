FROM centos:7.2.1511
MAINTAINER chengt "1630425@qq.com"

ENV TZ "Asia/Shanghai"

ENV LANG en_US.UTF-8  
ENV LANGUAGE en_US:en

RUN yum -y install yum-plugin-ovl

RUN yum -y install curl \
& yum -y install unzip \
& yum -y install vim* \

RUN yum -y install wget \
&& mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup \
&& wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo \
&& yum clean all \
&& yum makecache

CMD ["/bin/bash"]