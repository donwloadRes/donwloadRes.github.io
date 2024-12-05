---
layout: post
title: "win10 cuda11.8 和 torch2.0 安装指南"
date:   2021-10-08
tags: [CUDA,安装,11.8,cuDNN,环境]
comments: true
author: admin
---
# win10 cuda11.8 和 torch2.0 安装指南

本仓库提供了详细的步骤和说明文档，帮助您在Windows 10操作系统环境下安装CUDA 11.8和PyTorch 2.0。这一组合特别适用于那些需要在GPU环境下进行深度学习开发的用户。下面的步骤基于博主“小崔的技术博客”在CSDN上的文章指导，确保您的系统配置正确无误。

## 安装CUDA 11.8

1. **环境准备**：首先，建议在一个干净的Conda环境中操作，避免版本冲突。您可以创建一个新的环境并选择Python 3.11作为解释器。
   
2. **下载CUDA**：访问NVIDIA的官方网站，从archive部分找到CUDA 11.8的安装程序，并下载适合您系统的版本。

3. **安装过程**：运行下载的安装程序，按照向导指示进行安装。安装完毕需重启计算机。

4. **环境变量**：安装后，系统会自动添加CUDA_PATH和CUDA_PATH_V11_8环境变量。确保这两个变量指向正确的CUDA安装目录。

5. **验证CUDA**：通过命令行输入`nvcc -V`来验证CUDA是否安装成功。

## 安装CuDNN

1. 访问NVIDIA cuDNN官网，根据CUDA 11.8版本下载对应的cuDNN库。

2. 解压下载的文件，并将`bin`, `include`, `lib`目录下的文件复制到CUDA的安装目录下的相应位置，例如`C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.8`。

3. 更新PATH环境变量，包括cuDNN的相关目录。

## 安装PyTorch 2.0

1. **使用pip安装**：在确保CUDA和cuDNN已正确配置的环境中，运行以下pip命令来安装PyTorch 2.0与相应的torchvision和torchaudio：

   ```bash
   pip3 install numpy --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu118
   ```

2. **验证安装**：安装完成后，在Python环境下，可以通过导入torch并检查`.is_cuda`属性来验证GPU支持是否正常工作。

通过遵循以上步骤，您应该能够在Windows 10平台上成功设置CUDA 11.8和PyTorch 2.0环境，为深度学习项目奠定坚实的基础。记得在实际操作中细心对照每一步骤，确保每个环节都顺利完成。

## 下载链接

[win10cuda11.8和torch2.0安装指南](https://pan.quark.cn/s/6d08e20dda30)