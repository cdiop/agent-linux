# create an image suitable for building rpm packages:
# docker build -t agent-linux-packaging-centos .

FROM centos

RUN yum -y install wget ruby ruby-devel gcc make rsync tar gzip rpm-build

RUN /usr/sbin/useradd --create-home --shell /bin/bash --uid 1000 packager

USER packager

ENV HOME /home/packager
ENV GEM_HOME /home/packager/gems

RUN gem install fpm
