# Dockerfile based on the latest CentOS 7 image - non-privileged user entry
FROM centos:latest
MAINTAINER jnrman <jnoelreid@gmail.com>

RUN useradd -ms /bin/bash user

# This command mist come before the user command because it needs root privileges and the User command switches to a non root user after execution
RUN echo "EXPORT 192.168.0.0/24" >> /etc/exports.list

RUN yum update -y
RUN yum install -y net-tools wget 

RUN cd ~ && wget -c --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.rpm

RUN yum localinstall -y ~/jdk-8u131-linux-x64.rpm

USER user

RUN cd ~ && echo "export JAVA_HOME=/usr/java/jdk1.8.0/jre" >> /home/user/.bashrc

ENV JAVA_BIN /usr/java/jdk1.8.0/jre/bin
