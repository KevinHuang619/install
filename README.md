# install

## nvidia-driver and cuda 10.1
```shell
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt-get update
sudo apt-get install nvidia-418

#Command to verify installation
nvidia-smi
```

## miniconda

https://docs.conda.io/en/latest/miniconda.html#linux-installers

## docker

```shell
# enter container
docker exec -it <container name> /bin/bash
# run with gpu
nvidia-docker run --ipc=host ...
```

## pytorch
```shell
pip install torch==1.6.0+cu101 torchvision==0.7.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
```
