---
layout: post
title: "Linux更改本地离线镜像源RedHat 75  BCLinux 82"
date:   2020-03-16
tags: [挂载,ISO,yum,离线,镜像]
comments: true
author: admin
---
# 【Linux】更改本地离线镜像源（RedHat 7.5 & BCLinux 8.2）

本资源文件提供了详细的指南，帮助您在没有互联网连接的情况下，为您的Red Hat 7.5和BCLinux 8.2系统设置本地离线yum源。这对于需要在隔离网络环境中的服务器进行软件包安装和更新非常有用。

## 步骤概述：

### 对于Red Hat 7.5:

1. **下载ISO镜像**: 获取Red Hat 7.5的ISO镜像文件。
2. **创建挂载点**: 在根目录下创建`/media/rhel/`作为挂载点。
3. **修改YUM源**: 进入`/etc/yum.repos.d/`目录，备份现有源，并创建或编辑新的.repo文件（如`rhel-source.repo`），指定baseurl为本地镜像路径。
4. **挂载ISO**: 将ISO文件挂载至之前创建的挂载点。
5. **设置自动挂载**: 更新启动脚本(`/etc/rc.d/rc.local`)以实现系统启动时自动挂载。
6. **测试**: 使用`yum list`命令验证是否成功切换到了本地源。

### 对于BCLinux 8.2:

1. **ISO镜像准备**: 下载BCLinux 8.2的ISO镜像。
2. **创建挂载目录**: 例如，在`/data/media/`下创建对应目录。
3. **编辑YUM源**: 在`/etc/yum.repos.d/`下创建或调整.repo文件，如`BCLinux-AppStream.repo`，添加BaseOS与AppStream部分。
4. **挂载操作**: 将ISO文件挂载到指定目录，并确保配置正确。
5. **清理缓存与刷新**: 执行`yum clean all`与`yum makecache`。
6. **功能测试**: 安装一个软件包，如telnet，来确认离线源的有效性。

## 注意事项:

- 请根据实际ISO文件路径调整挂载命令中的路径。
- 确保在修改YUM源时关闭或停用原有的在线yum源，避免混淆。
- 自动挂载设置适用于需要长期保持离线状态的系统。
- 在执行任何系统级改动前，建议做好相应的系统备份。

通过以上步骤，您可以有效地在红帽及BCLinux系统上设置本地离线镜像源，简化软件包管理和维护工作。

## 下载链接

[Linux更改本地离线镜像源RedHat7.5BCLinux8.2](https://pan.quark.cn/s/ee88c2f8c5d6)