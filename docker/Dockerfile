FROM debian:latest

ENV DEBIAN_FRONTEND=noninteractive   \
    LANGUAGE=en_US.UTF-8 \
    LANG=en_US.UTF-8 \
    LC_ALL=en_US.UTF-8

RUN apt-get -yqq update \
 && apt-get -yqq install --no-install-recommends \
        build-essential \
        g++ \
        gcc \
        gfortran \
        make \
        gcovr \
 && rm -rf /var/lib/apt/lists/*

COPY . /build/


RUN cd /build/src && \
    make

ENV PATH=$PATH:/opt/demo/bin
