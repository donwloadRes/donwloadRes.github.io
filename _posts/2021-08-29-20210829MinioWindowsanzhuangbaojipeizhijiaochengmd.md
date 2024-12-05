---
layout: post
title: "Minio Windows 安装包及配置教程"
date:   2022-12-16
tags: [Minio,安装包,minio,key,解压]
comments: true
author: admin
---
# Minio Windows 安装包及配置教程

本仓库提供了一个Minio的Windows安装包，并附带详细的安装和配置教程。由于官网下载速度较慢，这里直接提供了安装包，方便大家快速获取并使用。

## 资源文件

- **文件名**: minio-windows-installer.zip
- **描述**: Minio的Windows安装包，包含安装和配置所需的文件。

## 安装步骤

1. **解压文件**: 将下载的`minio-windows-installer.zip`文件解压到任意目录。

2. **创建数据目录**: 在解压后的目录中创建一个名为`data`的文件夹，用于存放Minio的数据。

3. **添加执行权限**: 打开命令提示符（CMD），导航到解压后的目录，并执行以下命令：
   ```bash
   chmod +x minio
   ```

4. **后台启动Minio**: 在命令提示符中执行以下命令，以在后台启动Minio服务：
   ```bash
   nohup ./minio server ./data/ --console-address :8090 > nohup.out 2>&1 &
   ```

5. **配置Minio**: 启动后，Minio会在`data/`目录下生成一个名为`.minio.sys`的隐藏文件夹。打开该文件夹中的`config/config.json`文件，找到`access_key`和`secret_key`，分别对应用户名和密码。修改为所需的值，保存后退出。

6. **重启应用**: 修改配置文件后，重启Minio应用以使配置生效。

## 注意事项

- 请确保在执行命令时，路径和文件名正确无误。
- 配置文件中的`access_key`和`secret_key`是Minio的登录凭证，请妥善保管。

## 感谢

资源整理不易，如果本仓库对你有帮助，请给个赞哦！

## 下载链接

[MinioWindows安装包及配置教程](https://pan.quark.cn/s/93dc2bbee2f8)