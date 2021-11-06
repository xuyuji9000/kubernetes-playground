This file contains AKS(Azure Kubernetes Service) learning.

This file may be referenced by other files.

# Commands

- List the available regions

``` shell 
az account list-locations|less -i
```

- Create resource group


``` shell
az group create --location japanwest \
--name test-kx
```

- Create AKS

``` shell
az aks create --name test-kx \
--resource-group test-kx
```
