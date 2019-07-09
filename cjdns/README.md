# cjdns

Dockerfile and startup script is borrowed from [chpio's implementation](https://github.com/chpio/docker-cjdns),
with the main change being the latest non-slim Debian base image

The docker-compose file and the conf directory provide an example with three nodes,
connected in line `1--2--3`. Please note, that the example configuration includes private keys
and is not suitable for actually running cjdns nodes.

## How to run

You can use docker-compose to start the stack (which should build the image):

```sh
docker-compose up -d
```

or just build the image:

```sh
docker-compose build
```

If you don't want to use docker-compose, you can simply build the image using Docker only:

```sh
docker build -t vilunov/cjdns:latest .
```
