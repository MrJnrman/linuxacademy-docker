# Dockerfile based on the latest CentOS 7 image - non-privileged user entry
FROM centos:latest
MAINTAINER jnrman <jnoelreid@gmail.com>

RUN useradd -ms /bin/bash user

# ENTRYPOINT is different from CMD because it guarantees what will happen everytime a container is instantiated whether not a command is passed to the container and the creation point
ENTRYPOINT echo "This command will display this message on every container that is run from it"

USER user
