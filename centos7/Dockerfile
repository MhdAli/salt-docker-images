FROM centos:7

ADD saltstack-centos.repo /etc/yum.repos.d/salt-centos.repo

RUN rpm --import https://repo.saltstack.com/yum/redhat/7/x86_64/latest/SALTSTACK-GPG-KEY.pub
RUN yum -y install salt-minion net-tools &&\
    systemctl enable salt-minion

CMD ["/sbin/init"]
