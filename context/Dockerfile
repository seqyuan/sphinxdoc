#FROM sphinxdoc/sphinx
FROM alpine:latest

RUN apk update  && \
    apk add  --no-cache --update \
        gcc make automake gcc g++ python3 python3-dev cython freetype-dev
RUN pip3 install --upgrade pip

WORKDIR /docs
ADD requirements.txt /docs
ADD Makefile /docs

MAINTAINER Yuan Zan <seqyuan@gmail.com>

WORKDIR /docs

RUN make install 

ADD passwd /etc/
ADD group /etc/
