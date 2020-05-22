# Hand Detection VinAI Project
Dataset-Hand-Label and Training Centernet 

## Getting Started
Project Hand Detection in VinAI. Follow the instruction and training by your custom data  

## Installation
### Follow step by step 
* 1.[Cuda10.1](https://github.com/oggyfaker/Hand-Detection-VinAI/blob/master/Intro/Cuda10-1.md) 
* 2.[Anaconda](https://github.com/oggyfaker/Hand-Detection-VinAI/blob/master/Intro/Anaconda.md)
* 3.[CenterNet](https://github.com/oggyfaker/Hand-Detection-VinAI/blob/master/Intro/Centernet_setup.md)

## Running Demo 
### OBJECT DETECTION 
#### 1. Download model pretrain
* 1.[ctdet_coco_dla_2x](https://drive.google.com/file/d/1pl_-ael8wERdUREEnaIfqOV_VF2bEVRT/view)

#### 2. Run this command test 
```
cd /src 
python demo.py ctdet --demo webcam --load_model ../models/ctdet_coco_dla_2x.pth
```
