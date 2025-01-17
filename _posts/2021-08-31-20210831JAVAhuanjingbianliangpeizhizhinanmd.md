---
layout: post
title: "JAVA环境变量配置指南"
date:   2023-09-24
tags: [JAVA,java,环境变量,HOME%,配置]
comments: true
author: admin
---
# JAVA环境变量配置指南

本仓库提供了一个资源文件，帮助解决在配置JAVA环境变量时遇到的常见问题：“不是内部或外部命令，也不是可运行的程序或批处理文件”。

## 问题描述

在安装JAVA并配置环境变量后，有时在命令行中输入`javac`或`java`命令时，会遇到如下错误提示：

```
'javac' 不是内部或外部命令，也不是可运行的程序或批处理文件
```

或

```
'java' 不是内部或外部命令，也不是可运行的程序或批处理文件
```

## 解决方案

以下是解决该问题的详细步骤：

### 1. 卸载现有JAVA

首先，卸载当前计算机上已安装的JAVA。可以通过Windows自带的卸载程序来完成。

### 2. 重新安装JAVA

1. 在磁盘分区（如D盘）新建一个名为`java`的文件夹。
2. 在`java`文件夹下新建两个子文件夹，分别命名为`jdk`和`jre`。
3. 双击JAVA安装程序，安装过程中会有两次选择路径的机会：
   - 第一次选择JDK的安装路径，选择为`D:\java\jdk`。
   - 第二次选择JRE的安装路径，选择为`D:\java\jre`。

### 3. 配置环境变量

1. 右击“计算机”或“此电脑”，选择“属性”。
2. 点击“高级系统设置”，然后点击“环境变量”。
3. 在系统变量中进行以下配置：
   - 新建变量`JAVA_HOME`，变量值为`D:\java\jdk`。
   - 新建变量`CLASSPATH`，变量值为`%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar`。
   - 编辑变量`Path`，在变量值末尾添加`%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin`。

### 4. 测试配置

1. 打开命令提示符（cmd）。
2. 输入以下命令进行测试：
   - `java`
   - `javac`
   - `java -version`

如果以上命令均能正常执行并显示相关信息，则说明JAVA环境变量配置成功。

## 注意事项

- 确保JDK和JRE的安装路径不同，避免路径覆盖问题。
- 在配置环境变量时，注意路径的正确性和完整性。

通过以上步骤，您应该能够成功解决JAVA环境变量配置中的常见问题。如果仍有疑问，请参考相关文档或寻求技术支持。

## 下载链接

[JAVA环境变量配置指南](https://pan.quark.cn/s/09b1c9bb64f4)