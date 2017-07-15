# VERSION 1.0
FROM python:3.4.6-wheezy

RUN apt-get update \
 && apt-get -y install git graphviz-dev pkg-config vim-tiny \
 && cd /opt \
 && git clone -b develop https://github.com/sig9org/acitoolkit \
 && cd acitoolkit \
 && python setup.py install \
 && apt-get clean \
 && echo 'set paste' >> /root/.vimrc \
 && echo "alias ls='ls --color'" >> /root/.bashrc \
 && echo "export PS1='\[\033[01;36m\]atk-3.4.6\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '" >> /root/.bashrc
WORKDIR /opt/acitoolkit
CMD ["/bin/bash"]
