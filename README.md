# kubernetes-playground

# Commands

## minikube

- start cluster with cri-o runtime: `minikube start --container-runtime=cri-o`

## kubectl

- run nginx deployment: `kubectl run nginx --image=docker.io/nginx --port=80`

- expose service: `kubectl expose deployment nginx --type=NodePort`

- access service: `curl $(minikube service nginx --url)`