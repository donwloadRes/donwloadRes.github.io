---
layout: post
title: "Linux安装JDK 18并配置环境变量"
date:   2022-11-14
tags: [JDK,HOME,1.8,环境变量,安装]
comments: true
author: admin
---
# Linux安装JDK 1.8并配置环境变量

本资源文件提供了在Linux系统上安装JDK 1.8并配置环境变量的详细教程。通过本教程，您可以轻松地在Linux环境中设置Java开发环境，确保系统能够正确识别和使用JDK 1.8。

## 内容概述

1. **检查系统是否已安装JDK**  
   使用`java -version`命令检查系统是否已经安装了JDK。如果系统未安装JDK，则需要按照以下步骤进行安装。

2. **下载JDK 1.8**  
   提供两种下载方式：
   - 从Oracle官网下载JDK 1.8安装包。
   - 使用提供的百度网盘链接下载已备份的JDK 1.8安装包。

3. **创建JDK安装目录**  
   在`/usr/`目录下创建一个名为`java`的文件夹，用于存放JDK安装包。

4. **上传并解压JDK安装包**  
   将下载的JDK 1.8安装包上传至`/usr/java`文件夹，并使用`tar -zxvf`命令解压安装包。

5. **配置环境变量**  
   编辑`/etc/profile`文件，添加以下内容以配置`JAVA_HOME`、`JRE_HOME`、`CLASSPATH`和`PATH`环境变量：
   ```bash
   export JAVA_HOME=/usr/java/jdk1.8.0_241
   export JRE_HOME=$JAVA_HOME/jre
   export CLASSPATH=$JAVA_HOME/lib:$JRE_HOME/lib:$CLASSPATH
   export PATH=$JAVA_HOME/bin:$JRE_HOME/bin:$PATH
   ```

6. **使配置生效**  
   使用`source /etc/profile`命令使配置立即生效，或重新打开终端使配置生效。

7. **验证安装**  
   使用`java -version`和`echo $JAVA_HOME`命令验证JDK是否安装成功，并检查环境变量是否配置正确。

## 注意事项

- 如果系统自带OpenJDK，建议卸载或重新配置环境变量以使用下载的JDK 1.8。
- 确保在配置环境变量时，路径和版本号与实际安装的JDK版本一致。

通过本教程，您可以在Linux系统上顺利安装并配置JDK 1.8，为Java开发提供稳定的环境支持。

## 下载链接

[Linux安装JDK1.8并配置环境变量](https://pan.quark.cn/s/6e1ed3cd5063)