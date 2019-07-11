FROM nvidia/cuda:10.0-base-ubuntu18.04

WORKDIR /

ENV DEBIAN_FRONTEND noninteractive

RUN \
  apt-get update && \
  apt-get upgrade -y && \
  apt-get install -y \
    clang \
    libpython3-dev \
    libblocksruntime-dev \
    wget \
    libxml2 \
    gnupg && \
  rm -rf /var/lib/apt/lists/*
RUN \
  wget \
    https://storage.googleapis.com/swift-tensorflow-artifacts/releases/v0.4/rc2/swift-tensorflow-RELEASE-0.4-cuda10.0-cudnn7-ubuntu18.04.tar.gz && \
  tar xzf \
    swift-tensorflow-RELEASE-0.4-cuda10.0-cudnn7-ubuntu18.04.tar.gz && \
  rm -rf \
    swift-tensorflow-RELEASE-0.4-cuda10.0-cudnn7-ubuntu18.04.tar.gz

WORKDIR /work/
