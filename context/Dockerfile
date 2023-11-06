#FROM sphinxdoc/sphinx
continuumio/miniconda3:latest

WORKDIR /docs
ADD requirements.txt /docs
ADD Makefile /docs

MAINTAINER Yuan Zan <seqyuan@gmail.com>

WORKDIR /docs

RUN make install 

ADD passwd /etc/
ADD group /etc/
