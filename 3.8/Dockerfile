FROM ubuntu:trusty

RUN apt-get update
RUN apt-get install -yyy wget

RUN wget -O - http://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add -
COPY apt/llvm.list /etc/apt/sources.list.d/llvm.list
COPY apt/llvm.pref /etc/apt/preferences.d/llvm

RUN apt-get update
RUN apt-get upgrade -yyy
RUN apt-get install -yyy clang-3.8 libllvm3.8 libclang-3.8-dev llvm-3.8 llvm-3.8-tools zlib1g-dev libncurses5-dev

RUN apt-get install -yyy git cmake ccache

ENV PATH /usr/lib/llvm-3.8/bin:$PATH
