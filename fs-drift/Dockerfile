FROM centos/tools

USER root
WORKDIR /root/
RUN rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN yum install -y git python2-elasticsearch6 python2-redis python2-numpy
RUN git clone https://github.com/parallel-fs-utils/fs-drift
RUN git clone https://github.com/cloud-bulldozer/snafu /opt/snafu
