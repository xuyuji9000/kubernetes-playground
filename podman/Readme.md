This file contains the learning about podman.


# Commands

- Start podman

``` shell
# start the Podman-managed VM
podman machine init
podman machine start

# verify the installation information

podman info
```

- Build Docker image

``` shell
podman build -t podbuilt .

podman run podbuilt
```
