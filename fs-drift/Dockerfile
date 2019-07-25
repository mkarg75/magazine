FROM centos/tools

USER root
WORKDIR /root/
RUN yum install -y python2-elasticsearch python2-numpy python2-redis
RUN git clone https://github.com/parallel-fs-utils/fs-drift
RUN git clone https://github.com/cloud-bulldozer/snafu /opt/snafu
# if you want to run fs-drift as a distributed workload from 
# a single control point (like fio), with shared filesystem storage,
# use launch.sh as described in fs-drift documentation.
# if the environment variables for this pod aren't set
# then launch.sh will exit immediately and is a noop
RUN ln -sv /root/fs-drift/fs-drift-remote.py /usr/local/bin
CMD fs-drift/examples/docker/fs-drift/launch.sh
