---
layout: post
title: "使用rpm包及createrepo命令制作本地yum仓库"
date:   2021-12-14
tags: [rpm,createrepo,yum,仓库,bash]
comments: true
author: admin
---
# 使用rpm包及createrepo命令制作本地yum仓库

本文将详细介绍如何使用rpm包及createrepo命令制作本地yum仓库。通过这种方法，您可以在无法连接外网的生产环境中，快速安装所需的软件包及其依赖项。

## 1. 安装createrepo命令

### 1.1 外网环境
在外网环境中，您可以直接使用yum命令安装createrepo：
```bash
yum -y install createrepo
```

### 1.2 离线环境
在离线环境中，您可以使用提供的安装包进行安装：
```bash
rpm -ivh *rpm
```

## 2. 制作可配置yum源的yum仓库

### 2.1 准备rpm包
例如，您需要安装vim命令，通常需要用到以下几个包。将这些rpm包放到一个目录中。

### 2.2 生成仓库数据文件夹
在存放rpm包的目录下，使用createrepo命令生成一个仓库数据文件夹：
```bash
createrepo .
```

### 2.3 更新仓库
如果删除了rpm包或添加了新的rpm包，只需更新仓库即可：
```bash
createrepo --update .
```

## 3. 配置离线yum源

将生成的仓库数据文件夹复制到无法联网的生产环境中，并配置为离线的yum源。这样，您就可以使用yum命令安装vim及其他所需的软件包了。

通过以上步骤，您可以轻松地在无法连接外网的环境中，使用本地yum仓库安装所需的软件包及其依赖项。

## 下载链接

[使用rpm包及createrepo命令制作本地yum仓库](https://pan.quark.cn/s/6f8be24f7db5)