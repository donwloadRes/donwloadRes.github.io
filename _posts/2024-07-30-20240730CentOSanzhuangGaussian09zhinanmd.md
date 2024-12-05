---
layout: post
title: "CentOS 安装 Gaussian 09 指南"
date:   2023-08-22
tags: [bash,Gaussian,09,CentOS,g09]
comments: true
author: admin
---
# CentOS 安装 Gaussian 09 指南

## 简介
本资源文件提供了在 CentOS 系统上安装 Gaussian 09 的详细步骤。Gaussian 09 是一款广泛使用的量子化学计算软件，适用于分子能量和结构、过渡态能量和结构、化学键以及反应能量等研究。

## 安装步骤

### 1. 下载安装包
首先，需要下载 Gaussian 09 的安装包。由于某些原因，这里不提供具体的下载链接，有需要的小伙伴可以私信获取。

### 2. 解压文件
将下载好的文件进行解压：
```bash
tar -zxf G09_B01_LINUX_E64-930X.tgz
```
解压后，进入解压目录并设置文件权限：
```bash
cd g09
chmod -R 750 *
```

### 3. 配置环境变量
为了全局使用 Gaussian 09，需要配置环境变量。编辑 `/etc/profile` 文件：
```bash
vi /etc/profile
```
在文件末尾添加以下内容：
```bash
export g09root=/usr/local/gaussian
export GAUSS_EXEDIR=$g09root/g09
export GAUSS_SCRDIR=$g09root/tmp
export PATH=$PATH:$g09root/g09
```
保存并退出编辑器，然后执行以下命令使配置生效：
```bash
source /etc/profile
```

### 4. 计算测试
为了验证安装是否成功，可以进行一个简单的计算测试。首先，在 Windows 上使用 Gaussian View 创建一个水分子，并保存为 gif 文件，然后上传到服务器。

在服务器上创建输入和输出目录：
```bash
mkdir Input
mkdir Output
```
运行计算并输出结果：
```bash
cd Input
g09 <h2o.gif> ../Output/h2o.out
```

### 5. 查看结果
使用 `cat` 命令查看输出文件内容：
```bash
cd Output
cat h2o.out
```

## 注意事项
- 确保系统具备 root 权限。
- 安装过程中可能需要根据实际情况调整路径和文件名。
- 计算测试时，确保输入文件格式正确。

## 参考资料
本指南参考了 CSDN 博客文章，详细步骤和更多信息请参考原文。

---

通过以上步骤，您应该能够在 CentOS 系统上成功安装并运行 Gaussian 09。如有任何问题，欢迎交流讨论。

## 下载链接

[CentOS安装Gaussian09指南](https://pan.quark.cn/s/a6031b303913)