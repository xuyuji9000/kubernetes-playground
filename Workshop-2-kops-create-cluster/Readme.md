1. Prepare s3 bucket for storing states

    `aws s3 mb s3://test-kx-state-store`


2. Create cluster

    ``` bash
    export NAME=test-kx.k8s.local
    export KOPS_STATE_STORE=s3://test-kx-state-store
    kops create cluster --zones ap-southeast-1a $NAME
    ```

3. Login to master instance

    `ssh -i ~/.ssh/id_rsa admin@master-dns`

4. Control cluster from local

    ``` bash
    kops export kubecfg $NAME
    export NAME=test-kx.k8s.local
    kubectl get pods --all-namespaces
    ```
