# Solid Pod Demo

[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
[![Known Vulnerabilities](https://snyk.io/test/github/st3v3nhunt/solid-pod-demo/badge.svg)](https://snyk.io/test/github/st3v3nhunt/solid-pod-demo)

> Run through of the [Solid](https://solidproject.org/)
> [getting starting](https://solidproject.org/developers/tutorials/getting-started)
> guide

## Running the application

The application is Dockerised and can be run via `docker` or `docker compose`
commands. The easiest option is to use the `docker-compose` files and run the
application via `docker-compose up --build`. Alternatively, the same can be
achieved by building the image and running it with docker:

```shell
docker build . --build-arg NODE_ENV=development -t starter-node-repo

docker run --init -p 3000:3000 -p 9229:9229 -t starter-node-repo
```
