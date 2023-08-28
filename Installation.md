# CodeProject.AI windows docker Installation

### Install GPU drivers and cuda toolkit 

1. install nvidia gpu driver
- Install the CUDA 11.7 Drivers(Nvidia GPU drivers):

---
__https://www.nvidia.com/Download/index.aspx__

---

* Install the CUDA Toolkit 11.7:

---
https://developer.nvidia.com/cuda-11-7-0-download-archive?target_os=Windows&target_arch=x86_64

---

* Install CUDA Deep Neural Network (cuDNN)

---
https://www.codeproject.com/KB/Articles/5322557/install_CUDnn.zip

---

### Docker pull:
```cmd
docker --v

<pull cpu version >
docker pull codeproject/ai-server:latest

<pull gpu version>
docker pull codeproject/ai-server:gpu

<Simple Docker launch gpu >
docker run -d -p 32168:32168 --gpus all codeproject/ai-server:gpu

<Simple Docker launch cpu >
docker run -d -p 32168:32168 codeproject/ai-server:gpu





```


### Install docker engine on windows

Install  Windows Subsystem for Linux:
```cmd
wsl --install
```


Docker link for windows hosts download:

----
__https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=dd-smartbutton&utm_location=module___

----





01- install nvidia gpu driver (2 drivers)

02- install directx


03-install visual studio IDE

https://visualstudio.microsoft.com/

checkbox >>> Desktop develepment with C++


04- install nvidia toolkit

05- install nvidia cudnn script



































