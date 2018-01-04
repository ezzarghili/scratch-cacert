# ezzarghili/scratch-cacert
Docker scratch image with ca-certificates.crt from ubuntu based images mainly the ubuntu:lastet docker image

A daily build in an external CI is triggered to rebuild this repo at midnight UTC time, so if changes to ca-certicates from apt latest ubuntu image are available this repo will be updated.

We use this image mainly for golang single bin app to reduce the size of the generated image.

## usage

Example with executable binary `myAppBin`

```Dockerfile
FROM ezzarghili/scratch-cacert:latest
ADD myAppBin /
CMD ["/myAppBin"]
```
