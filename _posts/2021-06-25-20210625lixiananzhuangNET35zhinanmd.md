---
layout: post
title: "离线安装NET3.5指南"
date:   2021-07-14
tags: [NET3.5,安装,离线,Windows,安装包]
comments: true
author: admin
---
# 离线安装NET3.5指南

本仓库提供了一个离线安装NET3.5的资源文件，适用于Windows系统。通过本指南，您可以轻松完成NET3.5的离线安装。

## 安装准备

1. **确认Windows Update服务状态**：确保在服务中的Windows Update为运行状态（一般默认为运行状态）。
2. **下载NET3.5安装包**：根据您的系统版本，下载对应的NET3.5安装包。

## 安装步骤

1. **以管理员身份运行命令提示符**：
   - 按下 `Windows + R`，输入 `cmd`，然后按 `Ctrl + Shift + Enter` 以管理员身份运行。

2. **输入安装命令**：
   - 输入以下命令并回车：
     ```
     dism /online /enable-feature /featurename:netfx3 /Source:D:\sources\sxs
     ```
   - 其中 `D:\sources\sxs` 为NET3.5安装包对应的目录，请根据实际情况修改盘符。

3. **安装成功**：
   - 安装完成后，重新启动计算机即可。

## 常见问题解决

- **NetFx3ServerFeatures未启动**：
  - 输入以下命令启动NetFx3ServerFeatures：
    ```
    dism /online /enable-feature /featurename:NetFx3ServerFeatures
    ```

- **其他报错**：
  - 先删除已安装的高版本的NET，装好3.5后再安装高版本的NET。
  - （控制面板-程序和功能-启用或关闭windows功能 找到高版本的NET删除）

## 注意事项

- 安装过程中请确保系统盘有足够的空间。
- 如果遇到问题，请参考日志文件以便进一步诊断。

通过以上步骤，您可以顺利完成NET3.5的离线安装。如有任何问题，欢迎在仓库中提出。

## 下载链接

[离线安装NET3.5指南](https://pan.quark.cn/s/9c78e41c5e77)