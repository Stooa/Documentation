# Setup Local Environment

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

## Structure

This repository contains the Stooa code for:

### Backend

The `/backend` folder contains all the backend code. We are mainly using [Symfony][symfony] with [Api Platform][api-platform] (for the API generation) and [Sonata][sonata] for the administration panel.

If you change `backend` code, there are several checks that the code need to pass:
* `phpstan`
* `psalm`
* `php-cs-fixer`
* `phpunit`

### Frontend

The `/frontend` folder contains all the frontend code. We are mainly using [React][react] with [Next.js][next] and
[Apollo][apollo] for the GraphQL calls to the backend.

If you change `frontend` code, there are several checks that the code need to pass:
* `estlint`
* `jest tests`

## How to update Jitsi Meet Library manually ?

### Why manually?

We are using the official javascript jitsi meet library:

`https://github.com/jitsi/lib-jitsi-meet`

At the moment, the library is not uploaded to NPM packages. That's why we need to update the library manually.
This process will change once the official library is uploaded to NPM.

### How do we update the library manually?

Replacing the minified files locate at `fronted/public/vendor/` with the file names `lib-jitsi-meet.*`

### Example

To copy a specific version of the minified library, we will dot it from a Docker Jitsi Meet official image.

First, selecting a certain release in, for example `stable-6433`
`
https://github.com/jitsi/docker-jitsi-meet/releases
`

After that, we will create a temporary docker image to copy the minified file to our project:

```
docker run --name temp-container-name jitsi/web:stable-6433 /bin/true
docker cp temp-container-name:/usr/share/jitsi-meet/libs/lib-jitsi-meet.min.js frontend/public/vendor/lib-jitsi-meet.min.js
docker cp temp-container-name:/usr/share/jitsi-meet/libs/lib-jitsi-meet.min.map frontend/public/vendor/lib-jitsi-meet.min.map
docker rm temp-container-name
```

NOTE: The first command might give you some errors. However, this will not stop this from working.

[symfony]: https://github.com/symfony/symfony
[api-platform]: https://github.com/api-platform/api-platform
[sonata]: https://github.com/sonata-project/SonataAdminBundle
[react]: https://github.com/facebook/react
[next]: https://github.com/vercel/next.js/
[apollo]: https://github.com/apollographql