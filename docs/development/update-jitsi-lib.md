# How to update Jitsi Meet Library manually ?

## Project's package.json

We are using the official javascript jitsi meet library:

`https://github.com/jitsi/lib-jitsi-meet`

To use the library as a package we need to refer it to the release gzip, as they do in their jitsi-meet react application

## How do we update the library?

Replacing the link in the [package.json](https://github.com/Stooa/Stooa/blob/main/frontend/package.json) of the stooa's `frontend` app.

We use as reference the version used in [jitsi-meet](https://github.com/jitsi/jitsi-meet) which is the most stable version and used on their production web app.

**Where to get the link?** You can copy it from the [jitsi-meet](https://github.com/jitsi/jitsi-meet/blob/master/package.json) `package.json` or head to [lib-jitsi-meet repo releases](https://github.com/jitsi/lib-jitsi-meet/releases) and copy the .tgz link from the "Assets" in the release.

Link should look like this:\
https://github.com/jitsi/lib-jitsi-meet/releases/download/v1535.0.0%2Be6263e7c/lib-jitsi-meet.tgz

```json
"lib-jitsi-meet": "https://github.com/jitsi/lib-jitsi-meet/releases/download/v1529.0.0%2B669dbcbb/lib-jitsi-meet.tgz",
```
