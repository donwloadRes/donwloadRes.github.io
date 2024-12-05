---
layout: post
title: "Windows下快速安装Nginx并配置开机自动启动"
date:   2020-07-13
tags: [Nginx,nginx,Windows,开机,exe]
comments: true
author: admin
---
# Windows下快速安装Nginx并配置开机自动启动

本资源提供了详细的指南，旨在帮助用户在Windows操作系统上轻松安装Nginx，并配置其在系统启动时自动启动。Nginx作为一个高效且流行的Web服务器软件，在开发者和运维人员中极为常见，其简便的配置和强大的性能使其成为搭建网站和服务的理想选择。以下是简明的步骤概述：

### 安装Nginx

1. **下载Nginx**：首先，前往Nginx官方网站下载适合Windows版本的Nginx压缩包。
2. **解压文件**：将下载好的压缩包解压至您选择的目录，例如`D:\environment\nginx-1.24.0`。
3. **启动Nginx**：双击`nginx.exe`或者在解压目录下的命令行中执行`nginx.exe`或`start nginx`。

### 配置开机自动启动

为了实现Nginx的开机自启，我们将利用**Windows Service Wrapper**（WinSW）工具将Nginx作为Windows服务管理。

1. **下载WinSW**：访问GitHub或其他镜像站点下载WinSW，确保下载正确版本，适合您的Windows系统（x86或x64）。
2. **准备配置文件**：
   - 将下载的WinSW工具放置于Nginx安装目录，重命名为`nginx-service.exe`。
   - 创建`nginx-service.xml`配置文件，示例配置应包含Nginx的路径、日志位置等，具体内容需调整以匹配您的Nginx安装目录。
   
   ```xml
   <service>
     <id>nginx</id>
     <name>nginx</name>
     <description>Nginx Service</description>
     <executable>D:\your_path_to_nginx\nginx.exe</executable>
     <logpath>D:\your_path_to_nginx\logs</logpath>
     <logmode>roll</logmode>
     <startarguments>-p D:\your_path_to_nginx</startarguments>
     <stoparguments>-p D:\your_path_to_nginx -s stop</stoparguments>
   </service>
   ```

3. **注册为服务并配置开机启动**：
   - 打开命令提示符，使用管理员权限运行`nginx-service.exe install`命令。
   - 通过服务管理器设置该服务为开机自动启动。
   - 使用命令`sc config nginx start= auto`设置开机自动启动，或通过Windows服务界面手动配置。

完成上述步骤后，每当Windows启动时，Nginx将自动运行，无需人工干预，极大地提升了服务器管理的便利性。请根据实际情况调整路径和配置细节，以保证安装过程顺利进行。

## 下载链接

[Windows下快速安装Nginx并配置开机自动启动](https://pan.quark.cn/s/3d0eac573c51)