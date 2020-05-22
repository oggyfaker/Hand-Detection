# Hướng dẫn setup cho CenterNet
## Tạo thư mục chứa CenterNet và cocoapi

```
mkdir Vin 
cd /Vin 
git clone https://github.com/xingyizhou/CenterNet.git
git clone https://github.com/cocodataset/cocoapi.git
```
## Thay đổi file Functional
```
>>Cách 1<< 
sed -i "1254s/torch\.backends\.cudnn\.enabled/False/g" "anaconda/envs/{tên của env}/lib/python3.6/site-packages/torc/nn/functional.py"

>>Cách 2<<
Tìm file torch/nn/functional.py , dòng "torch.batch_norm" và replace "torch.backends.cudnn.enabled" thành "False"
```

## Cocoapi 
```
cd /cocoapi/PythonAPI
make
python setup.py install --user
```

## DCNv2 
```
# Down new DCNv2 

%cd /CenterNet/src/lib/models/networks/
sudo rm -rf DCNv2
git clone --recursive https://github.com/CharlesShang/DCNv2.git
(or)
git clone https://github.com/oggyfaker/DCNv2-CenterNet

# Make file 

cd /DCNv2
chmod +x make.sh
./make.sh
python setup.py build develop
```

## _Ext 
```
cd /CenterNet/src/lib/external
python setup.py install 
python setup.py build_ext --inplace
```
