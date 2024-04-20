FROM mcr.microsoft.com/devcontainers/base:jammy
COPY sysctl.80-vpp.conf /etc/sysctl.d/80-vpp.conf
COPY profile.99-vpp-dev.sh /etc/profile.d/99-vpp-dev.sh
RUN apt-get update
RUN apt-get install -y \
    chrpath \
    clang \
    cmake \
    curl \
    debhelper \
    dh-python \
    dpkg-dev \
    iputils-ping \
    libelf-dev \
    libnuma-dev \
    libpcap-dev \
    libssl-dev \
    m4 \
    nasm \
    ninja-build \
    pkg-config \
    python3-all \
    python3-ply \
    python3-setuptools \
    python3.11-venv \
    zlib1g-dev
ENV VPP_BUILD_DIR=/opt/vpp
RUN mkdir -p ${VPP_BUILD_DIR} && chown vscode ${VPP_BUILD_DIR}
