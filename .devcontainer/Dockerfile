#FROM mcr.microsoft.com/devcontainers/base:jammy
FROM ubuntu:focal
COPY sysctl.80-vpp.conf /etc/sysctl.d/80-vpp.conf
COPY profile.99-vpp-dev.sh /etc/profile.d/99-vpp-dev.sh
RUN useradd -u 1000 -m -k /etc/skel -s /bin/bash vscode
RUN apt-get -y update
RUN apt-get -y install git
RUN apt-get -y install make
RUN apt-get -y install sudo
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install tzdata
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install wireshark-common
RUN apt-get -y install iproute2
RUN apt-get -y install vim
RUN echo "vscode ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/vscode