FROM sphinxdoc/sphinx
#FROM python:3.7

RUN apt-get update -y && \
    apt-get install -y python3-pip wget

WORKDIR /docs
ADD requirements.txt /docs
ADD Makefile /docs

MAINTAINER Yuan Zan <seqyuan@gmail.com>

WORKDIR /docs

RUN make install 

ADD passwd /etc/
ADD group /etc/
