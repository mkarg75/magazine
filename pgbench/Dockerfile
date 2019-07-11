FROM centos/tools

USER root
RUN rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN rpm -ivh https://download.postgresql.org/pub/repos/yum/reporpms/EL-7-x86_64/pgdg-redhat-repo-latest.noarch.rpm
RUN yum -y update
RUN yum install -y postgresql-contrib
RUN yum install -y redis
RUN yum install -y python-elasticsearch
RUN yum install -y numpy
RUN git clone https://github.com/cloud-bulldozer/snafu /opt/snafu
