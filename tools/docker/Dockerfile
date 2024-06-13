FROM ubuntu:23.10
LABEL Name=ardour-vscode Version=0.0.1

ENV XARCH=x86_64
ENV ROOT=/build
ENV MAKEFLAGS=-j4

RUN sed -i '/deb-src/s/^# //' /etc/apt/sources.list && apt -y update

RUN apt -y install \
            wget \
            git \
            vim \
            python-is-python3 \
            gdb

RUN apt -y build-dep ardour
RUN apt -y install libjack-jackd2-dev

# see http://archive.ubuntu.com/ubuntu/pool/universe/a/ardour/ardour_7.5.0+ds-2.debian.tar.xz
