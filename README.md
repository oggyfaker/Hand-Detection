# Hand Detection VinAI Project
Dataset-Hand-Label and Training Centernet 
## Getting Started
1. Cài đặt môi trường Anaconda
2. Cài đặt Cuda 10.1 
3. Cài đặt Independence packed 
## 1. Cài đặt Anaconda 

## 2. Cài đặt cuda 10.1

```
# Nếu đã cài Cuda phiên bản khác , có thể xóa và cài lại 
sudo rm /etc/apt/sources.list.d/cuda*
sudo apt remove --autoremove nvidia-cuda-toolkit
sudo apt remove --autoremove nvidia-*
```
```
# Them file PPA 
sudo apt update

sudo add-apt-repository ppa:graphics-drivers/ppa

sudo apt-key adv --fetch-keys  http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub

sudo bash -c 'echo "deb http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64 /" > /etc/apt/sources.list.d/cuda.list'

sudo bash -c 'echo "deb http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64 /" > /etc/apt/sources.list.d/cuda_learn.list'
```
```
# Cuda 10.1 
sudo apt update
sudo apt install cuda-10-1
sudo apt install libcudnn7
```
```
# Chinh sua file path và thêm câu lệnh này vào cuối dòng file profile  
sudo gedit ~/.profile

if [ -d "/usr/local/cuda-10.1/bin/" ]; then
    export PATH=/usr/local/cuda-10.1/bin${PATH:+:${PATH}}
    export LD_LIBRARY_PATH=/usr/local/cuda-10.1/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
fi
```
```
# Check 
nvidia-smi
nvcc  – version

/sbin/ldconfig -N -v $(sed ‘s/:/ /’ <<< $LD_LIBRARY_PATH) 2>/dev/null | grep libcudnn
```

