# Setup and run development environment

## Requirements

To run this project, you need to have:

- [Git](https://git-scm.com/)
- [Nvm](https://github.com/nvm-sh/nvm)
- [NPM](https://www.npmjs.com/)
- [Mkcert](https://github.com/FiloSottile/mkcert)
- [Docker](https://www.docker.com/)
- [Docker compose](https://docs.docker.com/compose/cli-command/)

## How to run this project?

The only command you should use to run this project is:

```
make up
```

This commands builds the `docker-compose.yaml` file. As you can see, it contains containers
related to Jitsi (JVB, Jicofo, Prosody), backend (nginx, fpm, consumer) and frontend (nginx, next).
There are other commands to control the Docker containers, you can find them on `Makefile`.

In case of mysql error table/view doesn't exist, run `make provision`.

## How to enable Xdebug?

After the initial `make up`, you can run:

```
make up-debug
```

To disable it again, just run `make up`.

### Access

There are several endpoints configured for Stooa:

* https://localhost:8343 (Access to the frontend)
* https://localhost:8443 (Access to the backend)
* https://localhost:8443/docs (Access to the docs)
* https://localhost:8443/admin (Access to the backoffice)
* http://localhost:8025 (Access to Mailhog)

## Running frontend outside Docker

There are some cases where Docker does no perform good enough (mostly when using Docker for Mac / Windows).
For those cases you can run the frontend outside Docker. We recommend using Nvm, since it will allow you
to use the same Node version as if it was running with Docker.

There are some steps you need to run:

```
cd frontend

# This one might prompt you to install the required
# Node version if you don't have it already
nvm use

npm clean-install

npm dev
```

### Access

All the other accesses remain the same (even the frontend running inside Docker), but the frontend will 
also be accesible through:

* http://localhost:3000
