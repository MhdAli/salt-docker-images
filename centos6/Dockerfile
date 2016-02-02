FROM centos:6

ADD saltstack-centos.repo /etc/yum.repos.d/salt-centos.repo

RUN rpm --import https://repo.saltstack.com/yum/redhat/6/x86_64/latest/SALTSTACK-GPG-KEY.pub
RUN yum -y install salt-minion &&\
    chkconfig --add salt-minion

CMD ["/sbin/init"]
