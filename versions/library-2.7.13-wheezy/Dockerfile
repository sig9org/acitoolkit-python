# VERSION 1.0
FROM python:2.7.13-wheezy

RUN apt-get update \
 && apt-get -y install git graphviz-dev pkg-config vim-tiny \
 && cd /opt \
 && git clone -b develop https://github.com/sig9org/acitoolkit \
 && git clone https://github.com/datacenter/acitoolkit \
 && cd acitoolkit \
 && python setup.py install \
 && apt-get clean
ADD vimrc /root/.vimrc
WORKDIR /opt/acitoolkit
CMD ["/bin/bash"]
