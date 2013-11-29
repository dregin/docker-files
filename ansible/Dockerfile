FROM ubuntu:12.10
MAINTAINER dregin dregin@gmail.com

RUN apt-get update
RUN apt-get install -y python-pip python-dev python-setuptools git curl
RUN git clone https://github.com/dotcloud/docker-py.git;\
	cd docker-py;\
	python setup.py install

RUN pip install ansible
ADD https://raw.github.com/cove/docker-ansible/master/docker-ansible.py /usr/share/ansible/docker
RUN chmod 755 /usr/share/ansible/docker
