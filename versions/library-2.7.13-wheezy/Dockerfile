# VERSION 1.0
FROM python:2.7.13-wheezy

RUN apt-get update \
 && apt-get -y install git graphviz-dev pkg-config vim-tiny \
 && cd /opt \
 && git clone -b develop https://github.com/sig9org/acitoolkit \
 && cd acitoolkit \
 && python setup.py install \
 && apt-get clean \
 && echo 'set paste' >> /root/.vimrc \
 && echo 'ls --color' >> /root/.bashrc \
 && export PS1='\[\033[01;36m\]acitoolkit-2.7.13\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
ADD vimrc /root/.vimrc
WORKDIR /opt/acitoolkit
CMD ["/bin/bash"]
