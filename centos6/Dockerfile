FROM centos:6

ADD saltstack-centos.repo /etc/yum.repos.d/salt-centos.repo

RUN rpm --import https://repo.saltstack.com/yum/redhat/6/x86_64/latest/SALTSTACK-GPG-KEY.pub && \
    rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-6.noarch.rpm
RUN yum -y install salt-minion python-pip &&\
    chkconfig --add salt-minion &&\
    easy_install pbr && \
    easy_install testinfra

ENV container=docker

CMD ["/sbin/init"]
