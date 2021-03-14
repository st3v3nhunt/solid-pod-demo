# Solid Pod Demo

[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
[![Known Vulnerabilities](https://snyk.io/test/github/st3v3nhunt/solid-pod-demo/badge.svg)](https://snyk.io/test/github/st3v3nhunt/solid-pod-demo)

> Run through of the [Solid](https://solidproject.org/)
> [getting starting](https://solidproject.org/developers/tutorials/getting-started)
> guide

## Running the application

### Local host

The easiest way to run the application is on the local host machine, first
install the modules, then run parcel. The following commands should do it:

```shell
npm install
npm run parcel
```

And the application will be available at
[http://localhost:1234](http://localhost:1234)

### Docker

Note on running the application with Docker. Parcels Hot Module Reloading (HMR)
doesn't work currently as the communication is done via WebSockets on what
looks like a randomly allocated port and only ports 1234 and 9229 have been
mapped. This should be a solvable problem but I've not looked into it, hence
the suggestion to run on directly on the machine.

The application is Dockerised and can be run via `docker` or `docker compose`
commands. The easiest option is to use the `docker-compose` files and run the
application via `docker-compose up --build`. Alternatively, the same can be
achieved by building the image and running it with docker:

```shell
docker build . --build-arg NODE_ENV=development -t starter-node-repo

docker run --init -p 1234:1234 -p 9229:9229 -t starter-node-repo
```
