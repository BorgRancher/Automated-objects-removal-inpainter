# Remove-objects-pytorch

Automated object remover Inpainter is a project that combines Semantic segmentation and EdgeConnect arhitectures with minor changes in order to remove specified object/s from photos. For Semantic Segmentation, the code from pytorch has been adapted, whereas for EdgeConnect, the code has been adapted from [https://github.com/knazeri/edge-connect](https://github.com/knazeri/edge-connect).

This project is capable of removing objects from list of 20 different ones.

Python 3.7.7 and pytorch 1.5.1 have been used in this project.

<img src="https://user-images.githubusercontent.com/31131069/89242660-188c8e80-d5d0-11ea-8277-1ed6b9a0f83d.png" width="30%"></img> <img src="https://user-images.githubusercontent.com/31131069/89242666-1cb8ac00-d5d0-11ea-83b0-61c86d26fa68.png" width="30%"></img> <img src="https://user-images.githubusercontent.com/31131069/89242673-1fb39c80-d5d0-11ea-8ac4-906b5d06d4d6.png" width="30%"></img> <img src="https://user-images.githubusercontent.com/31131069/89242684-25a97d80-d5d0-11ea-9756-811189856ae4.png" width="30%"></img> <img src="https://user-images.githubusercontent.com/31131069/89242689-28a46e00-d5d0-11ea-9041-70bd16103d17.png" width="30%"></img> <img src="https://user-images.githubusercontent.com/31131069/89242695-2b9f5e80-d5d0-11ea-8c72-c865cc72616b.png" width="30%"></img> <img src="https://user-images.githubusercontent.com/31131069/89242813-6b664600-d5d0-11ea-9125-276610c10bda.png" width="30%"></img> <img src="https://user-images.githubusercontent.com/31131069/89242821-6f926380-d5d0-11ea-997b-005e5875471a.png" width="30%"></img> <img src="https://user-images.githubusercontent.com/31131069/89242827-728d5400-d5d0-11ea-9776-e3392312e774.png" width="30%"></img> 

## How does it work?

Semantic segmenator model of deeplabv3/fcn resnet 101 has been combined with EdgeConnect. A pre-trained segmentation network has been used for object segmentation (generating a mask around detected object), and its output is fed to a EdgeConnect network along with input image with portion of mask removed. EdgeConnect uses two stage adversarial architecture where first stage is edge generator followed by image completion network. EdgeConnect paper can be found [here](https://arxiv.org/abs/1901.00212) and code in this [repo](https://github.com/knazeri/edge-connect)



## Prerequisite
* python 3
* pytorch 1.0.1 <
* NVIDIA GPU + CUDA cuDNN (optional)

## Installation
