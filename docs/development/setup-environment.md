# Setup development environment

## Requirements

To run this project, you need to have:

- [Git](https://git-scm.com/)
- [Nvm](https://github.com/nvm-sh/nvm)
- [Yarn](https://yarnpkg.com/)
- [Mkcert](https://github.com/FiloSottile/mkcert)
- [Docker](https://www.docker.com/)

## How to run this project?

The only command you should use to run this project is:

```
make up
```

This commands builds the `docker-compose.yaml` file. As you can see, it contains containers
related to Jitsi (JVB, Jicofo, Prosody), backend (nginx, fpm, consumer) and frontend (nginx, next).
There are other commands to control the Docker containers, you can find them on `Makefile`.

In case of mysql error table/view doesn't exist, run `make provision`.

## Access

There are several endpoints configured for Stooa:

* https://localhost:8343 (Access to the frontend)
* https://localhost:8443 (Access to the backend)
* https://localhost:8443/docs (Access to the docs)
* https://localhost:8443/admin (Access to the backoffice)
* http://localhost:8025 (Access to Mailhog)
