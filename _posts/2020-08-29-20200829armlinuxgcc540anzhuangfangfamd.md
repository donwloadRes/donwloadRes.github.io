---
layout: post
title: "armlinuxgcc540 安装方法"
date:   2020-01-19
tags: [arm,linux,gcc,5.4,bash]
comments: true
author: admin
---
# arm-linux-gcc-5.4.0 安装方法

## 简介
本资源文件提供了 arm-linux-gcc-5.4.0 的安装方法，适用于需要在 Ubuntu 系统上安装该交叉编译工具链的用户。

## 安装步骤

### 1. 下载安装包
- 可以通过百度搜索下载 arm-linux-gcc-5.4.0 的安装包。
- 也可以使用提供的百度云盘链接下载（提取码：734w）。

### 2. 安装步骤
1. 进入 `/usr/local` 文件路径下，并创建一个新文件夹 `arm-linux-gcc`，并赋予其最高权限：
   ```bash
   mkdir arm-linux-gcc
   chmod 777 arm-linux-gcc
   ```

2. 将 arm-linux-gcc-5.4.0 安装包复制到 `arm-linux-gcc` 文件夹中：
   ```bash
   cp arm-linux-gcc-5.4.0.tar.gz /usr/local/arm-linux-gcc
   ```

3. 解压安装包：
   ```bash
   tar xzvf arm-linux-gcc-5.4.0.tar.gz
   ```

4. 解压后会出现一个名为 `5.4.0` 的新文件夹。

5. 修改 `/etc/profile` 文件的属性（默认是只读属性，修改成可读可写）。

6. 在 `/etc/profile` 文件的末尾添加以下内容：
   ```bash
   export PATH=/usr/local/arm-linux-gcc/5.4.0/bin:$PATH
   ```

7. 将文件属性再修改回去（防止误操作）：
   ```bash
   sudo chmod 644 profile
   ```

8. 更新 `profile` 文件内容：
   ```bash
   source /etc/profile
   ```

9. 检查是否成功安装：
   ```bash
   echo $PATH
   ```
   若出现 `/usr/local/arm-linux-gcc/5.4.0/bin` 的字样，则表示安装成功。也可以使用以下命令查看版本信息：
   ```bash
   arm-linux-gcc -v
   ```

10. arm-linux-gcc-5.4.0 安装完成。

## 注意事项
- 确保系统环境符合安装要求。
- 安装过程中可能需要管理员权限。
- 安装完成后，建议重启系统以确保环境变量生效。

## 参考资料
- 更多详细信息可以参考提供的 CSDN 博客文章。

## 下载链接

[arm-linux-gcc-5.4.0安装方法](https://pan.quark.cn/s/470d6e2a7647)