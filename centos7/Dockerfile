FROM centos:7

ADD saltstack-centos.repo /etc/yum.repos.d/salt-centos.repo

RUN rpm --import https://repo.saltstack.com/yum/redhat/7/x86_64/latest/SALTSTACK-GPG-KEY.pub && \
    rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
RUN yum -y install salt-minion net-tools python-pip &&\
    systemctl enable salt-minion && \
    pip install testinfra

ENV container=docker

CMD ["/sbin/init"]
