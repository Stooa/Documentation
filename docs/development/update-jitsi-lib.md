# How to update Jitsi Meet Library manually ?

## Why manually?

We are using the official javascript jitsi meet library:

`https://github.com/jitsi/lib-jitsi-meet`

At the moment, the library is not uploaded to NPM packages. That's why we need to update the library manually.
This process will change once the official library is uploaded to NPM.

## How do we update the library manually?

Replacing the minified files locate at `fronted/public/vendor/` with the file names `lib-jitsi-meet.*`

## Example

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
