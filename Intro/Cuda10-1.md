# Installation of Cuda 10.1 Ubuntu 18.04

## Delete the old driver (if installed) 
```
# Nếu đã cài Cuda phiên bản khác , có thể xóa và cài lại 

sudo rm /etc/apt/sources.list.d/cuda*

sudo apt remove --autoremove nvidia-cuda-toolkit

sudo apt remove --autoremove nvidia-*
```
## Install driver and Cuda 10.1
```
sudo add-apt-repository -y ppa:graphics-drivers/ppa

sudo apt -y update

sudo apt -y upgrade

sudo apt -y install nvidia-driver-435
(sudo reboot now)

wget http://developer.download.nvidia.com/compute/cuda/10.1/Prod/local_installers/cuda_10.1.243_418.87.00_linux.run

sudo sh cuda_10.1.243_418.87.00_linux.run

# Trường hợp lỗi không có gpu
sudo gedit ~/.bashrc
export PATH=/usr/local/cuda-10.1/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-10.1/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
source ~/.bashrc

```
## Test
```
nvidia-smi
```
