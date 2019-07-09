FROM buildpack-deps:buster as builder

WORKDIR /build/
RUN \
  apt-get update -y && \
  apt-get upgrade -y && \
  apt-get install --no-install-recommends -y nodejs
RUN \
  git clone https://github.com/cjdelisle/cjdns.git cjdns --depth 1 --branch cjdns-v20.3 && \
  cd cjdns && \
  ./do


FROM debian:buster

COPY start-cjdns /usr/bin/
COPY --from=builder /build/cjdns/cjdroute/ /usr/bin/

CMD ["start-cjdns"]
