# Install Enviroment

## Install Anaconda
```
cd /tmp
curl -O https://repo.anaconda.com/archive/Anaconda3-2019.03-Linux-x86_64.sh
bash Anaconda3-2019.03-Linux-x86_64.sh
```

## Create env
```
conda create -n CenterNet python=3.6 

conda install pytorch=1.4.0 torchvision cudatoolkit=10.1 -c pytorch ( -c python) 

%cd CenterNet 
pip install -r "requirements.txt" 

pip install matplotlib
pip install progress

```
