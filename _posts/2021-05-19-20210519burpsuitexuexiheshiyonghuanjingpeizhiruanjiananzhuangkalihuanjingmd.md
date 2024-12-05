---
layout: post
title: "burpsuite学习和使用环境配置软件安装kali环境"
date:   2021-09-26
tags: [Burp,Suite,usr,bin,Java]
comments: true
author: admin
---
# burpsuite学习和使用-环境配置软件安装（kali环境）

本资源仓库提供了详细的指南，专为希望在Kali Linux环境下配置和使用Burp Suite的网络安全研究者和渗透测试人员准备。Burp Suite是一款强大的Web应用程序安全测试工具，特别适用于发现和利用Web应用的安全漏洞。以下是安装和配置Burp Suite的专业版步骤，确保您的Kali系统能够顺利运行这一必备工具。

## 环境要求

- **操作系统**: Kali Linux
- **Java版本**: JDK 8，因为某些版本的Burp Suite可能与较新版本的Java兼容性不佳。
- **Burp Suite**: 选用专业版，以解锁更多高级功能。

## 安装步骤概览

### 1. 卸载旧版本Burp Suite（可选）
如果您之前已经安装了社区版或其他版本的Burp Suite，可以通过以下命令卸载：
```
sudo apt remove burpsuite
```

### 2. 查看Kali系统位数
确保下载正确的Java和Burp Suite版本：
```bash
uname -m
```

### 3. Java安装
下载并配置Java Development Kit 8：
- 从Oracle官网或提供的链接下载JDK 8。
- 解压并配置环境变量：
    - 解压命令：`tar -zxf jdk-8u411-linux-x64.tar.gz`
    - 移动至 `/usr/local/`：`sudo mv jdk1.8.0_411 /usr/local/`
    - 编辑环境变量：通过 `sudo vi /etc/profile` 并添加以下内容：
        ```
        JAVA_HOME=/usr/local/jdk1.8.0_411
        PATH=$PATH:$HOME/bin:$JAVA_HOME/bin
        export JAVA_HOME
        export PATH
        ```
    - 更新替代选项并设置默认Java：
        ```bash
        update-alternatives --install "/usr/bin/java" "java" "/usr/local/jdk1.8.0_411/bin/java" 1
        update-alternatives --set java /usr/local/jdk1.8.0_411/bin/java
        ```

### 4. Burp Suite专业版安装
- 下载Burp Suite专业版压缩包。
- 解压并将Burp Suite移到 `/usr/bin` 目录。
- 运行激活脚本，按照指示完成激活过程。

### 5. 快捷方式配置
- 创建一个可执行的Shell脚本以便快速启动Burp Suite，并在KDE或GNOME桌面上建立快捷方式。

### 6. 浏览器代理设置
- 配置您的浏览器使用Burp Suite作为代理，通常端口号为8080，以便捕获和分析流量。

## 注意事项
- 确保每一步骤中的路径和文件名与您下载的实际文件匹配。
- 根据实际需要调整JDK版本和Burp Suite的版本号。
- 遵循版权和许可协议，在使用激活工具时谨慎行事，合法使用软件。

这篇指南详细记录了从环境准备到完全配置Burp Suite professional在Kali Linux上的每个步骤，帮助您迅速建立一个高效的工作环境。记得在安装和配置过程中仔细检查每一步的输出，确保没有遗漏任何关键设置。

## 下载链接

[burpsuite学习和使用-环境配置软件安装kali环境](https://pan.quark.cn/s/2cee23eb2095)