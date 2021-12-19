# Introduction

This is a simple "Hello World" service example.

Also this example is based on AKS.

# Version

AKS: v1.20.9


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

4. Apply kubernetes configuration

``` shell
kubectl apply -f ./k8s/deployment.yaml
kubectl apply -f ./k8s/service.yaml
```

5. Smoke test

``` shell
# smoke test with an Alpine pod
kubectl run --rm=true --restart=Never -it --image=alpine bash
```
