FROM rust:1.37.0-buster

WORKDIR /work/
VOLUME /work/
EXPOSE 8888

RUN \
  apt-get update && \
  apt-get install -y \
    pkg-config \
    libzmq3-dev \
    jupyter-console \
    jupyter-notebook && \
  cargo install evcxr_jupyter && \
  evcxr_jupyter --install

CMD ["jupyter-notebook", "--ip=0.0.0.0"]
