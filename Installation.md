# CodeProject.AI windows docker Installation

* https://www.codeproject.com/ai/docs/faq/windows-installer.html

### Install docker engine on windows

Install  Windows Subsystem for Linux:
```bat
wsl --install
```


Docker link for download:

----
__https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=dd-smartbutton&utm_location=module___

----

### Install GPU drivers and cuda toolkit:







```

# cpu version
docker pull codeproject/ai-server:latest


# gpu version
docker pull codeproject/ai-server:gpu




# Simple Docker launch (settings saved in the container)
docker run --name CodeProject.AI -d -p 32168:32168 codeproject/ai-server


docker run --name CodeProject.AI -d -p 32168:32168 codeproject/ai-server:gpu --gpus all


# Advanced Docker launch (settings saved outside of the container)

docker run --name CodeProject.AI -d -p 32168:32168 ^
 --mount type=bind,source=C:\ProgramData\CodeProject\AI\docker\data,target=/etc/codeproject/ai ^
 --mount type=bind,source=C:\ProgramData\CodeProject\AI\docker\modules,target=/app/modules ^
   codeproject/ai-server


# To use the GPU enabled images

docker run --name CodeProject.AI -d -p 32168:32168 --gpus all ^
 --mount type=bind,source=C:\ProgramData\CodeProject\AI\docker\data,target=/etc/codeproject/ai ^
 --mount type=bind,source=C:\ProgramData\CodeProject\AI\docker\modules,target=/app/modules ^
   codeproject/ai-server:gpu


GPU is not being used
Please ensure you have the NVidia CUDA drivers installed:

Install the CUDA 11.7 Drivers
Install the CUDA Toolkit 11.7.

Download and run our cuDNN install script.
https://www.codeproject.com/KB/Articles/5322557/install_CUDnn.zip


