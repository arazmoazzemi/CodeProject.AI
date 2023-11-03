# CodeProject.AI windows docker Installation 😄🤠

### Install GPU drivers and cuda toolkit 

---
1. Install the Nvidia Latest GPU Drivers:

- [CUDA 11.7 Drivers](https://www.nvidia.com/Download/index.aspx)

- [Directx installation is optional](https://download.microsoft.com/download/1/7/1/1718CCC4-6315-4D8E-9543-8E28A4E18C4C/dxwebsetup.exe)

---

2. Install the CUDA 11.7 Toolkit:

- [CUDA 11.7 Toolkit](https://developer.nvidia.com/cuda-11-7-0-download-archive?target_os=Windows&target_arch=x86_64)

---

3. Install CUDA Deep Neural Network with script(cuDNN):

- [cuDNN](https://www.codeproject.com/KB/Articles/5322557/install_CUDnn.zip)

---

4. Install visual studio IDE:

- [Visual Studio](https://visualstudio.microsoft.com/)

- Install   __Desktop develepment with C++__  section

---

### Install docker engine on windows

### ***Add repository for docker engine:***

```cmd
edit C:/Users/Username/.docker/machine/default/config.json
add the registry : "InsecureRegistry": ["x.x.x.x:port"]


Example :
add the registry : "registry-mirrors": ["https://docker.host:5000"]

restart docker (see comment below)*
restart windows (there must be a better way ;-)
docker login x.x.x.x:port
```


Install  Windows Subsystem for Linux:
```cmd
wsl --install
```
- [Install docker engine for windows](https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=dd-smartbutton&utm_location=module)

----

## Docker commands:
[Help](https://hub.docker.com/r/codeproject/ai-server)


```cmd
docker --v
```

Install  CodeProject.AI **cpu** version:
```cmd
docker pull codeproject/ai-server:latest
```

### Use gpu:💪
```cmd
docker run -d -p 32168:32168 --gpus all codeproject/ai-server:latest
```

Install  CodeProject.AI **gpu** version:
```cmd
docker pull codeproject/ai-server:gpu
```

Simple Docker launch gpu:
```cmd
docker run -d -p 32168:32168 --gpus all codeproject/ai-server:gpu
```

Simple Docker launch cpu:
```cmd
docker run -d -p 32168:32168 codeproject/ai-server:gpu
```
----



### [Setting up Facial Recognition in Blue Iris](https://www.codeproject.com/Articles/5348246/CodeProject-AI-Server-Blue-Iris-and-Face-Recogniti)




---

### MotionEye

[Download MotionEye ISO](https://github.com/motioneye-project/motioneyeos/releases)

[Raspberry Pi MotioneyeOS with BlueIris Security](https://photobyte.org/raspberry-pi-motioneyeos-with-blueiris-security)

---

http://192.168.0.123:8081

MotionEye stream in BlueIris, you need to add a new camera and make the following settings in the video configuration panel:

```config
Address: Use http:// 192.168.0.123:8081* NB: Use your Pi IP address!
User: admin and password empty
Make: Generic/ONVIF
Model: MJPEG stream
Media/video/RTSP port: 8081
Video Main stream: /mjpeg.cgi
```

---

### BlueIris Hikvision IPCAM Stream Example:
```config
Main : /Streaming/Channels/1
Sub : /Streaming/Channels/2
```
---

### BlueIris KDT IPCAM Stream Example:
```config
Main : /mode=real&idc=1&ids=1
Sub : /mode=real&idc=1&ids=2
```

---









