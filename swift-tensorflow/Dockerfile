FROM ubuntu:18.04

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
    gnupg && \
  rm -rf /var/lib/apt/lists/*
RUN \
  wget \
    https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-repo-ubuntu1804_10.1.105-1_amd64.deb && \
  dpkg -i cuda-repo-ubuntu1804_10.1.105-1_amd64.deb && \
  apt-key adv --fetch-keys \
    https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub && \
  apt-get update && \
  apt-get install -y cuda-10-0 && \
  rm -rf \
    cuda-repo-ubuntu1804_10.1.105-1_amd64.deb \
    /var/lib/apt/lists/*
RUN \
  wget \
    https://storage.googleapis.com/s4tf-kokoro-artifact-testing/versions/v0.2/rc3/swift-tensorflow-RELEASE-0.2-cuda10.0-cudnn7-ubuntu18.04.tar.gz && \
  tar xzf \
    swift-tensorflow-RELEASE-0.2-cuda10.0-cudnn7-ubuntu18.04.tar.gz && \
  rm -rf \
    swift-tensorflow-RELEASE-0.2-cuda10.0-cudnn7-ubuntu18.04.tar.gz

WORKDIR /work/

