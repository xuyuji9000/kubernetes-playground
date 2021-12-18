# Setup

1. Build container image

``` shell
podman build . -t yogiman/hello-world
```

2. Run container

``` shell
podman run -P yogiman/hello-world
```

3. Push container image to image registry


``` shell
podman push yogiman/hello-world
```
