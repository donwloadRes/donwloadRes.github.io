---
layout: post
title: "Maven 3.5.4 安装与配置指南"
date:   2024-10-30
tags: [Maven,3.5,xml,下载,路径]
comments: true
author: admin
---
# Maven 3.5.4 安装与配置指南

本资源文件提供了Maven 3.5.4的安装和配置指南，帮助开发者快速上手并配置Maven环境。以下是详细的安装和配置步骤。

## 一、安装Maven 3.5.4

1. **下载Maven压缩包**：
   - 可以从官网下载Maven 3.5.4的压缩包，或者使用提供的下载链接。
   - 下载链接：[Maven 3.5.4 下载链接](此处不提供具体链接)

2. **解压Maven压缩包**：
   - 将下载的`apache-maven-3.5.4`压缩包解压到你选择的文件夹中。
   - 注意：路径中不要包含中文，以避免潜在的问题。

## 二、配置环境变量

1. **设置MAVEN_HOME**：
   - 右击“此电脑” -> 属性 -> 高级系统设置 -> 环境变量。
   - 新建环境变量，变量名为`MAVEN_HOME`，变量值为Maven解压的路径（例如：`G:\Java_\KU\apache-maven-3.5.4`）。

2. **配置Path变量**：
   - 在系统变量中找到`Path`，点击编辑，添加`%MAVEN_HOME%\bin`。

## 三、配置settings.xml文件

1. **复制settings.xml文件**：
   - 将压缩包中的`settings.xml`文件复制到Maven解压路径下。
   - 同时，将该文件复制到`C:\Users\你的用户名\.m2`目录下。

## 四、测试Maven安装

1. **验证安装**：
   - 打开命令提示符（cmd），输入`mvn -v`。
   - 如果显示Maven版本信息，说明安装成功。

## 五、配置IDEA中的Maven

1. **设置Maven路径**：
   - 打开IDEA，进入设置（Settings），搜索Maven。
   - 在Maven home path中填写Maven的安装路径。

2. **配置本地仓库路径**：
   - 如果本地仓库路径不在D盘，需要在`settings.xml`文件中修改`localRepository`路径。

## 六、导包到本地仓库

1. **在pom.xml中添加依赖**：
   - 在项目的`pom.xml`文件中添加所需的依赖项。
   - 例如：
     ```xml
     <dependencies>
         <dependency>
             <groupId>org.jsoup</groupId>
             <artifactId>jsoup</artifactId>
             <version>1.14.1</version>
         </dependency>
         <dependency>
             <groupId>mysql</groupId>
             <artifactId>mysql-connector-java</artifactId>
             <version>5.1.25</version>
         </dependency>
     </dependencies>
     ```

2. **等待依赖下载**：
   - 添加依赖后，Maven会自动下载所需的库到本地仓库。
   - 下载完成后，可以在本地仓库路径中查看已下载的库。

通过以上步骤，你已经成功安装并配置了Maven 3.5.4，并可以在项目中使用Maven进行依赖管理和构建。

## 下载链接

[Maven3.5.4安装与配置指南](https://pan.quark.cn/s/9c92d2b252e0)