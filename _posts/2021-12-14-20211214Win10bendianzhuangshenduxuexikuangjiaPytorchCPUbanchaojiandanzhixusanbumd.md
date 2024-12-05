---
layout: post
title: "Win10本地安装深度学习框架PytorchCPU版超简单只需三步
date   20230112
tags whlPytorch安装cp38文件
comments true
author admin

 Win10本地安装深度学习框架PytorchCPU版超简单只需三步

 简介
本资源文件提供了一个详细的指南帮助你在Windows 10系统上本地安装深度学习框架Pytorch的CPU版本整个过程仅需三步操作简单适合初学者

 安装步骤

 第一步检查支持的whl文件类型
在命令提示符cmd中输入以下代码查看你的电脑支持的whl文件类型

python m pip debug verbose

运行后你会看到支持的whl文件类型请务必记录下这些信息以便后续下载正确的whl文件

 第二步下载相应的whl文件
根据第一步中查看到的支持的whl文件类型下载对应的Pytorch whl文件如果你使用的是Python 38版本可以直接从提供的百度网盘地址提取相应文件如果是其他版本的Python请访问官方网站下载对应版本的whl文件

 第三步安装Pytorch
1 以管理员身份打开命令提示符并进入whl文件所在的目录
2 输入以下两行代码进行安装
   
   pip install torch180cpucp38cp38winamd64whl
   pip install torchvision090cpucp38cp38winamd64whl"
date:   2023-01-12
tags: [whl,Pytorch,安装,cp38,文件]
comments: true
author: admin
---
# Win10本地安装深度学习框架Pytorch（CPU版），超简单只需三步！！！

## 简介
本资源文件提供了一个详细的指南，帮助你在Windows 10系统上本地安装深度学习框架Pytorch的CPU版本。整个过程仅需三步，操作简单，适合初学者。

## 安装步骤

### 第一步：检查支持的whl文件类型
在命令提示符（cmd）中输入以下代码，查看你的电脑支持的whl文件类型：
```
python -m pip debug --verbose
```
运行后，你会看到支持的whl文件类型。请务必记录下这些信息，以便后续下载正确的whl文件。

### 第二步：下载相应的whl文件
根据第一步中查看到的支持的whl文件类型，下载对应的Pytorch whl文件。如果你使用的是Python 3.8版本，可以直接从提供的百度网盘地址提取相应文件。如果是其他版本的Python，请访问官方网站下载对应版本的whl文件。

### 第三步：安装Pytorch
1. 以管理员身份打开命令提示符，并进入whl文件所在的目录。
2. 输入以下两行代码进行安装：
   ```
   pip install "torch-1.8.0+cpu-cp38-cp38-win_amd64.whl"
   pip install "torchvision-0.9.0+cpu-cp38-cp38-win_amd64.whl"
   ```
   安装完成后，Pytorch和torchvision将成功安装在你的系统中。

## 验证安装
1. 打开Python环境，输入以下代码导入Pytorch：
   ```
   import torch
   ```
   如果导入成功，说明Pytorch已正确安装。
2. 运行以下代码验证Pytorch的功能：
   ```
   x = torch.rand(2, 3)
   print(x)
   ```
   如果输出一个2x3的随机数矩阵，说明Pytorch安装成功并可以正常使用。

## 注意事项
- 请确保在安装过程中以管理员身份运行命令提示符，以避免权限问题。
- 如果遇到下载速度慢的问题，可以尝试使用镜像源或手动下载whl文件。

通过以上三步，你就可以在Windows 10系统上成功安装并使用Pytorch的CPU版本了。希望这个指南对你有所帮助！

## 下载链接

[Win10本地安装深度学习框架PytorchCPU版超简单只需三步](https://pan.quark.cn/s/9228090292d1)