# Libtorch on Arm64

## Libtorch for Arm64

Download [pytorch 1.7.0 for arm64 here](http://mathinf.com/pytorch/arm64/torch-1.7.0a0-cp37-cp37m-linux_aarch64.whl)
Download [torch vision 0.8 for arm64 here](http://mathinf.com/pytorch/arm64/torchvision-0.8.0a0+45f960c-cp37-cp37m-linux_aarch64.whl)

And unzip to `libtorch-1.7`. The `libtorch-arm` contains `lib` and `include` folder from `libtorch-1.7` for C libraries only.

## Build 

```bash

sudo docker build -t sugarme/libtorch-1.7.0-cpu:arm64 -f ./Dockerfile-arm64-cpu .
sudo docker push sugarme/libtorch-1.7.0-cpu:arm64

```

## Test

```bash
sudo docker container run -it --name=torch-cpu-arm64 sugarme/libtorch-1.7.0-cpu:arm64 /bin/bash

```






## References
1. http://mathinf.com/pytorch/arm64/
2. https://forums.developer.nvidia.com/t/pytorch-for-jetson-version-1-8-0-now-available/72048
3. https://discuss.pytorch.org/t/libtorch-for-raspberry-pi/63107
