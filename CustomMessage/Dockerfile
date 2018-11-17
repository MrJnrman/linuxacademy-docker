# Dockerfile based on the latest CentOS 7 image - non-privileged user entry
FROM centos:latest
MAINTAINER jnrman <jnoelreid@gmail.com>

RUN useradd -ms /bin/bash user

# This command mist come before the user command because it needs root privileges and the User command switches to a non root user after execution
RUN echo "EXPORT 192.168.0.0/24" >> /etc/exports.list

USER user

