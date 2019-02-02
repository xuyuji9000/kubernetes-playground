
``` bash
kubectl apply -f ./jenkins
helm install --name jenkins -f helm/jenkins-values.yaml stable/jenkins --namespace jenkins-project
```

- Delete helm chart

    `helm delete --purge jenkins`

# Reference 

1. [Deploy Jenkins with dynamic slaves on Minikube](https://itnext.io/deploy-jenkins-with-dynamic-slaves-in-minikube-8aef5404e9c1)
