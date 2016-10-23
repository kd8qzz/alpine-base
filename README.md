# Alpine docker base image
Alpine base image with sane default configs. This tries to balance the easier usage but to stay as minimal as possible.
This image weights: `8.098 MB`.

## Base image with slap commandline editor
`onnimonni/alpine-base:slap` contains edge version of alpine with [slap](https://github.com/slap-editor/slap) command line editor.
This is for the devs who don't feel that nano/vim are productive.

Available in docker hub: [onnimonni/alpine-base](https://hub.docker.com/r/onnimonni/alpine-base/).

This image uses [s6-overlay](https://github.com/just-containers/s6-overlay/#the-docker-way).

The image contains:
* @testing and @community packages already aliased for apk
* envsubst and few other helpers preinstalled
* Timezone set to Europe/Helsinki
* ll,la,l aliases included for easier debugging while attached to docker container

The container has custom `validate_sha256sum` script which is used to check if downloaded scripts have corrupted, changed or MITMed.

## License
MIT
