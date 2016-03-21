FROM centos:7

# SaltStack repo
RUN rpm --import https://repo.saltstack.com/yum/redhat/7/x86_64/latest/SALTSTACK-GPG-KEY.pub
ADD saltstack.repo /etc/yum.repos.d/saltstack.repo

# EPEL repo
RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm

# Install SaltStack and GitFS
RUN yum -y install salt-master salt-ssh salt-minion python-pygit2 GitPython python-dulwich python-pip
RUN pip install testinfra

# Install tools
RUN yum -y install vim

VOLUME ["/etc/salt/ssh-key"]

CMD ["salt-master", "-linfo"]
