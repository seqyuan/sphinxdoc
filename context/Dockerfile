#FROM sphinxdoc/sphinx
FROM amazonlinux:latest

RUN yum update -y && \
		yum install -y python3 python3-devel texlive-xetex wget


WORKDIR /docs
ADD requirements.txt /docs
ADD Makefile /docs

MAINTAINER Yuan Zan <seqyuan@gmail.com>

WORKDIR /docs

RUN make install 

ADD passwd /etc/
ADD group /etc/
