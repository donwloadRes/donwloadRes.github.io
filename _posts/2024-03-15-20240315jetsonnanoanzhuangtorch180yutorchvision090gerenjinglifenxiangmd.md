---
layout: post
title: "jetsonnano安装torch180与torchvision090个人经历分享"
date:   2024-12-02
tags: [安装,PyTorch,torchvision,CUDA,Jetson]
comments: true
author: admin
---
# jetsonnano安装torch1.8.0与torchvision0.9.0（个人经历分享）

欢迎阅读这份详细的指南，它记录了在Jetson Nano设备上安装PyTorch 1.8.0与torchvision 0.9.0的全过程，适合遇到同样挑战的开发者参考。本资源是基于博主亲身经历整理而成的血泪史，旨在帮助您避免遇到相同的坑。

## 介绍

本指南针对那些希望在Jetson Nano上部署深度学习项目，特别是计划使用YOLOv5模型的朋友们。由于特定硬件和环境要求，直接使用pip安装往往不能满足CUDA的兼容性需求，因此，正确安装指定版本的PyTorch和torchvision至关重要。

## 系统需求

- **硬件平台**：Jetson Nano
- **CUDA版本**：建议使用与您的JetPack版本相匹配的CUDA，如CUDA 10.2
- **Python环境**：Python 3.6 (依据您的系统配置可能有所不同)
- **目标库版本**：
  - PyTorch 1.8.0
  - Torchvision 0.9.0

## 安装步骤概览

1. **准备工作**：确保已安装Archiconda3或相应的Python虚拟环境。
2. **下载资源**：从可靠来源获取PyTorch 1.8.0的`.whl`文件和torchvision的安装脚本及其依赖。
3. **依赖安装**：使用`apt-get`安装必要的依赖库，如`libopenmpi2`, `libopenblas-dev`, `libjpeg-dev`, 和 `zlib1g-dev`。
4. **安装PyTorch**：通过pip直接安装下载的PyTorch `.whl`文件。
5. **特殊处理torchvision**：手动安装torchvision，可能需要调整环境变量以解决编译错误。
6. **CUDA环境设置**：修正CUDA Home路径，确保正确指向 `/usr/local/cuda`，可能需要编辑`.bashrc`文件并source使其生效。
7. **克服编译错误**：跟随文档中提供的解决策略，比如修改环境变量，确保NVCC的正确调用。

## 注意事项

- 在执行`setup.py install`前确保在正确的torchvision源码目录下，并且已经安装所有必需的依赖。
- 修改环境变量时，小心操作，以免影响其他CUDA应用。
- 重启环境或终端会话，有时候是解决问题的关键步骤之一。

## 结论

通过上述步骤，您可以成功地在Jetson Nano上部署PyTorch 1.8.0和torchvision 0.9.0，为您的项目奠定坚实的基础。记住，耐心和仔细是解决技术难题的重要钥匙。如果遇到具体技术障碍，不妨参考社区资源或者此篇文章中提及的方法，持续尝试直到成功。

请注意，安装过程中涉及的具体命令和软件版本可能会随时间变化，请务必验证最新的兼容性和软件更新。祝您安装过程顺利！

---

此README.md提供了一个简洁明了的指南，旨在帮助读者快速理解如何在Jetson Nano上安装必要的深度学习库。

## 下载链接

[jetsonnano安装torch1.8.0与torchvision0.9.0个人经历分享分享](https://pan.quark.cn/s/bc0ba8f5d9e2)