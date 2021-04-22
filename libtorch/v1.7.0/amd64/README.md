# Libtorch C++ Docker Image


## Build 

```bash

sudo docker build -t sugarme/libtorch-1.7.0-cpu:amd64 -f ./Dockerfile-cpu .
sudo docker push sugarme/libtorch-1.7.0-cpu:amd64

sudo docker build -t sugarme/libtorch-1.7.0-cu110:amd64 -f ./Dockerfile-cu110 .
sudo docker push sugarme/libtorch-1.7.0-cu110:amd64

```

## Test

```bash
sudo docker container run -it --name=torch-cpu sugarme/libtorch-1.7.0-cpu:amd64 /bin/bash

sudo docker container run --gpus all -it --name=torch-gpu sugarme/libtorch-1.7.0-cu110:amd64 /bin/bash
```

