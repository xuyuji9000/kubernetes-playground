
- Deploy

    ``` bash
    kubectl apply -f ./jenkins
    helm install --name jenkins -f helm/jenkins-values.yaml stable/jenkins --namespace jenkins-project
    # First time get admin user password
    printf $(kubectl get secret --namespace jenkins-project jenkins -o jsonpath="{.data.jenkins-admin-password}" | base64 --decode);echo
    ```


- Upgrade

    `helm upgrade jenkins stable/jenkins -f helm/jenkins-values.yaml --namespace jenkins-project`

- Delete

    ``` bash
    kubectl delete -f ./jenkins
    helm delete --purge jenkins
    ```


- Delete helm chart

    `helm delete --purge jenkins`

# Reference 

1. [Deploy Jenkins with dynamic slaves on Minikube](https://itnext.io/deploy-jenkins-with-dynamic-slaves-in-minikube-8aef5404e9c1)

2. [Jenkins Helm Chart](https://github.com/helm/charts/tree/master/stable/jenkins)

