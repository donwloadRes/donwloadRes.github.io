---
layout: post
title: "树莓派4B部署yolov5安装torch180torchvision090
date   20220312
tags torchtorchvision安装树莓4B
comments true
author admin

 树莓派4B部署yolov5安装torch180torchvision090

本仓库提供了一个资源文件用于在树莓派4B上部署yolov5并安装torch180和torchvision090以下是详细的安装步骤和说明

 资源文件内容

 torch180torchvision090cp37cp37mlinuxarmv7lwhl适用于树莓派4B的torch和torchvision预编译包

 安装步骤

1 下载资源文件
   从本仓库下载torch180torchvision090cp37cp37mlinuxarmv7lwhl文件

2 安装依赖
   在树莓派上安装必要的依赖库
   bash
   sudo aptget update
   sudo aptget install python3pip
   

3 安装torch和torchvision
   使用pip安装下载的预编译包
   bash
   pip3 install torch180torchvision090cp37cp37mlinuxarmv7lwhl
   

4 验证安装
   安装完成后可以通过以下命令验证torch和torchvision是否安装成功
   bash
   python3 c import torch printtorchversion
   python3 c import torchvision printtorchvisionversion"
date:   2022-03-12
tags: [torch,torchvision,安装,树莓,4B]
comments: true
author: admin
---
# 树莓派4B部署yolov5：安装torch1.8.0+torchvision0.9.0

本仓库提供了一个资源文件，用于在树莓派4B上部署yolov5，并安装torch1.8.0和torchvision0.9.0。以下是详细的安装步骤和说明。

## 资源文件内容

- `torch-1.8.0+torchvision-0.9.0-cp37-cp37m-linux_armv7l.whl`：适用于树莓派4B的torch和torchvision预编译包。

## 安装步骤

1. **下载资源文件**：
   从本仓库下载`torch-1.8.0+torchvision-0.9.0-cp37-cp37m-linux_armv7l.whl`文件。

2. **安装依赖**：
   在树莓派上安装必要的依赖库：
   ```bash
   sudo apt-get update
   sudo apt-get install python3-pip
   ```

3. **安装torch和torchvision**：
   使用pip安装下载的预编译包：
   ```bash
   pip3 install torch-1.8.0+torchvision-0.9.0-cp37-cp37m-linux_armv7l.whl
   ```

4. **验证安装**：
   安装完成后，可以通过以下命令验证torch和torchvision是否安装成功：
   ```bash
   python3 -c "import torch; print(torch.__version__)"
   python3 -c "import torchvision; print(torchvision.__version__)"
   ```

## 注意事项

- 确保树莓派的操作系统为Raspbian Buster或更高版本。
- 如果遇到安装问题，请参考[CSDN博客文章](https://blog.csdn.net/qq_44166630/article/details/119647498)获取更多帮助。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个资源文件。

## 下载链接

[树莓派4B部署yolov5安装torch1.8.0torchvision0.9.0](https://pan.quark.cn/s/e974bf66b61e)