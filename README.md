# Workshop-1 Start a nginx container with minikube

# Commands

## minikube

- start cluster with cri-o runtime: `minikube start --container-runtime=cri-o`

## kubectl

- run nginx deployment: `kubectl run nginx --image=docker.io/nginx --port=80`

- expose service: `kubectl expose deployment nginx --type=NodePort`

- access service: `curl $(minikube service nginx --url)`





## Reference

1. [Running Kubernetes Locally via Minikube](https://kubernetes.io/docs/setup/minikube/#alternative-container-runtimes)
