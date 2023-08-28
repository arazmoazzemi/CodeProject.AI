# CodeProject.AI windows docker Installation 😄

### Install GPU drivers and cuda toolkit 

---
1. Install the Nvidia Latest GPU Drivers:

- [CUDA 11.7 Drivers](https://www.nvidia.com/Download/index.aspx)

- [Directx installatin is optional](https://download.microsoft.com/download/1/7/1/1718CCC4-6315-4D8E-9543-8E28A4E18C4C/dxwebsetup.exe)

---

2. Install the CUDA 11.7 Toolkit:

- [CUDA 11.7 Toolkit](https://developer.nvidia.com/cuda-11-7-0-download-archive?target_os=Windows&target_arch=x86_64)

---

3. Install CUDA Deep Neural Network with script(cuDNN):

- [cuDNN](https://www.codeproject.com/KB/Articles/5322557/install_CUDnn.zip)

---

4. install visual studio IDE

- [Visual Studio](https://visualstudio.microsoft.com/)

- Install   __Desktop develepment with C++__  section

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



































