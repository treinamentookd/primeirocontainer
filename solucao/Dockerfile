FROM centos:centos8

LABEL maintainer="Seu Nome / E-mail"

RUN yum update -y && \
      yum install -y git && \
      yum install -y java-11-openjdk-devel.x86_64 && \
      yum clean all

RUN cd /opt && \
      curl -O https://downloads.apache.org/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz && \
      tar -xzvf apache-maven-3.6.3-bin.tar.gz && \
      export PATH=$PATH:/opt/apache-maven-3.6.3/bin

RUN git clone https://github.com/treinamentookd/primeirocontainer.git

RUN cd primeirocontainer/fonte && \
      mvn clean install
