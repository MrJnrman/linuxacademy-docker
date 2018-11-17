# Dockerfile based on the latest CentOS 7 image - non-privileged user entry
FROM centos:latest
MAINTAINER jnrman <jnoelreid@gmail.com>

RUN useradd -ms /bin/bash user

CMD "echo" "This is a custom container message"

USER user
