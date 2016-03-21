FROM debian:jessie

RUN apt-get update \
 && apt-get -y install wget \
 && wget -O - https://repo.saltstack.com/apt/debian/8/amd64/latest/SALTSTACK-GPG-KEY.pub | apt-key add - \
 && echo "deb http://repo.saltstack.com/apt/debian/8/amd64/latest jessie main" >> /etc/apt/mirror.list

RUN apt-get update \
 && apt-get -y install salt-minion net-tools python-pip \
 && systemctl enable salt-minion

ENV container=docker

RUN pip install testinfra

CMD ["/sbin/init"]
