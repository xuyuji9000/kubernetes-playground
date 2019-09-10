- Create role binding

``` bash
kubectl create rolebinding allow-jenkins-work-on-default-namespace \
--role=jenkins \
--serviceaccount=jenkins:jenkins
```

- Deploy Jenkins: `kubectl apply -n jenkins -f ./service.yaml`
