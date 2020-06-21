FROM  centos:latest

RUN  yum install sudo -y
RUN  yum install  wget -y
RUN      sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins.io/redhat-stable/jenkins.repo  
RUN  sudo rpm --import http://pkg.jenkins.io/redhat-stable/jenkins.io.key 
RUN  yum install jenkins  -y
RUN  yum install java-11-openjdk.x86_64   -y
RUN  sudo  yum install  /sbin/service  -y
RUN  sudo yum install net-tools -y
RUN  sudo yum install python36 -y
RUN  sudo yum install  httpd -y
RUN  sudo yum install  git  -y
RUN  sudo yum install  vim -y
RUN  touch /etc/yum.repos.d/docker.repo
COPY  docker.repo  /etc/yum.repos.d/
RUN  yum install docker-ce --nobest --skip-broken -y


EXPOSE 8080

CMD  sudo /etc/rc.d/init.d/jenkins start  && /bin/bash

#service  jenkins start -DFOREGROUND  
