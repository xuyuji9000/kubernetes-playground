- start cluster with cri-o runtime: `minikube start`

- open dashboard: `minikube dashboard`

- access service: `curl $(minikube service nginx --url)`

- access pod: `kubectl exec -it POD_NAME /bin/bash`

## Reference

1. [Running Kubernetes Locally via Minikube](https://kubernetes.io/docs/setup/minikube/#alternative-container-runtimes)
