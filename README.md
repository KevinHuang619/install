# install

## nvidia-driver and cuda 10.1

```shell
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt-get update
sudo apt-get install nvidia-418

# install cuda10.1 if need
wget https://developer.nvidia.com/compute/cuda/10.1/Prod/local_installers/cuda-repo-ubuntu1604-10-1-local-10.1.105-418.39_1.0-1_amd64.deb
sudo dpkg -i cuda-repo-ubuntu1604-10-1-local-10.1.105-418.39_1.0-1_amd64.deb
sudo apt-key add /var/cuda-repo-10-1-local-10.1.105-418.39/7fa2af80.pub
sudo apt-get update
sudo apt-get install cuda

#Command to verify installation
nvidia-smi

# install nvcc
sudo apt-get install nvidia-cuda-toolkit
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
## soft link

```shell
ln -s /home/jupyter/Development/pantheon-lab/library/ stylegan2/
```
