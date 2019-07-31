- run postgres container:

``` bash
docker run --rm \
-p 5432:5432 \
-e POSTGRES_PASSWORD=example postgres 
```

- Access database: `psql -h localhost -U postgres`

- Start a ubuntu container: `kubectl run -it --rm centos  --image=centos  /bin/bash`

