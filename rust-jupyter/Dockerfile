FROM rust:1.33.0-stretch

RUN \
  apt-get update && \
  apt-get install -y \
    pkg-config \
    libzmq3-dev \
    jupyter-notebook && \
  cargo install evcxr_jupyter && \
  evcxr_jupyter --install

WORKDIR /work/
VOLUME /work/

CMD ["jupyter-notebook", "--ip=0.0.0.0"]

