FROM centos/tools

USER root
RUN rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN curl -s https://copr.fedorainfracloud.org/coprs/ndokos/pbench/repo/epel-7/ndokos-pbench-epel-7.repo > /etc/yum.repos.d/copr-pbench.repo
RUN yum --enablerepo=ndokos-pbench install -y pbench-fio
RUN yum install -y git python-pip
RUN pip install --upgrade pip
RUN pip install elasticsearch numpy configparser statistics
RUN git clone https://github.com/cloud-bulldozer/snafu /opt/snafu
