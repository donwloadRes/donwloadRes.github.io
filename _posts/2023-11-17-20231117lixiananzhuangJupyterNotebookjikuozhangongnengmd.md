---
layout: post
title: "离线安装 Jupyter Notebook 及扩展功能"
date:   2022-11-07
tags: [安装,Jupyter,Notebook,命令提示符,离线]
comments: true
author: admin
---
# 离线安装 Jupyter Notebook 及扩展功能

本仓库提供了一个资源文件，用于离线安装 Jupyter Notebook 及其扩展功能。通过本资源文件，您可以在没有网络连接的环境中成功安装和配置 Jupyter Notebook。

## 资源文件内容

- **whls 文件夹**：包含所有依赖包的 `.whl` 文件。
- **requirements.txt**：列出了需要安装的具体包名和版本。

## 安装步骤

1. **解压安装包**：将下载的资源文件解压到 Python 安装目录的 `Scripts` 文件夹下（或其他指定目录）。
2. **打开命令提示符**：以管理员权限打开命令提示符（cmd）。
3. **切换目录**：使用 `cd` 命令切换到解压后的 `Scripts` 文件夹。
4. **安装依赖包**：在命令提示符中输入以下命令并回车：
   ```
   pip install --no-index --no-dependencies --upgrade --find-links=whls -r requirements.txt
   ```
5. **验证安装**：安装完成后，输入 `pip list` 查看已安装的包。确认 `jupyter` 及其相关组件已成功安装。
6. **启动 Jupyter Notebook**：在命令提示符中输入 `jupyter notebook`，启动 Jupyter Notebook。

## 注意事项

- 确保解压目录与 Python 安装目录的 `Scripts` 文件夹一致，以避免安装命令的细微差异。
- 如果在安装过程中遇到问题，请检查 `requirements.txt` 文件中的包名和版本是否正确。

通过以上步骤，您可以在离线环境中成功安装并使用 Jupyter Notebook 及其扩展功能。

## 下载链接

[离线安装JupyterNotebook及扩展功能](https://pan.quark.cn/s/aa577d2c1d85)