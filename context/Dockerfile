FROM sphinxdoc/sphinx

WORKDIR /docs
ADD requirements.txt /docs
ADD Makefile /docs

MAINTAINER Yuan Zan <seqyuan@gmail.com>

WORKDIR /docs

RUN python3 -m pip install -r requirements.txt

RUN make install 

ADD passwd /etc/
ADD group /etc/
