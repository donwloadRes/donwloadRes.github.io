---
layout: post
title: "JavaFX+SpringBoot2.7+JDK17+Launch4j+InnoSetup实现JVMTI的Jar包加密-H2数据"
date:   2024-02-08
tags: [加密,编译,Jar,JavaFX,序列号]
comments: true
author: admin
---
# JavaFX+SpringBoot2.7+JDK17+Launch4j+InnoSetup实现JVMTI的Jar包加密/H2数据

## 项目描述

本项目是一个综合性的Java应用示例，结合了JavaFX、Spring Boot、JDK 17、Launch4j和InnoSetup等技术，实现了Jar包加密、H2数据库加密以及安装时的序列号在线校验等功能。通过本项目，您可以学习如何将JavaFX的界面框架与Spring Boot的业务框架无缝集成，并实现一系列的安全性和功能性增强。

## 主要功能

1. **JavaFX界面框架**：采用JavaFX作为前端界面框架，并结合了Atlantafx和Ikonli图标库，实现了自定义主题。
2. **Spring Boot后端框架**：使用Spring Boot 2.7.5版本，结合MyBatis 2.1.2版本，实现了业务逻辑的处理和数据库操作。
3. **Jar包加密**：通过JVMTI技术，实现了对Jar包的加密，增强了应用的安全性。
4. **H2数据库加密**：对H2数据库进行了加密处理，保护数据的安全性。
5. **安装时序列号校验**：在安装过程中，会提示用户输入软件序列号，并通过RESTful接口进行在线校验。
6. **一键编译脚本**：提供了`build.py`脚本文件，支持Python 3环境，通过该脚本可以一键编译并生成Windows安装程序。

## 项目结构

- **src/main/java**：包含Java源代码，包括JavaFX界面、Spring Boot业务逻辑、MyBatis配置等。
- **src/main/resources**：包含配置文件、数据库脚本等资源文件。
- **dll项目工程**：提供了用于Jar包加密的DLL项目工程，需安装Visual Studio进行编译。
- **build.py**：一键编译脚本，支持Python 3环境，可生成Windows安装程序。

## 使用说明

1. **环境准备**：
   - JDK 17
   - Python 3
   - Visual Studio（用于编译DLL项目）

2. **编译DLL**：
   - 打开`dll项目工程`，使用Visual Studio进行编译，生成Jar包加密所需的DLL文件。

3. **运行build.py**：
   - 在项目根目录下运行`build.py`脚本，该脚本会自动编译项目并生成Windows安装程序。

4. **安装程序**：
   - 生成的安装程序会提示输入软件序列号，序列号通过RESTful接口进行在线校验。

## 注意事项

- 本项目依赖于JDK 17，请确保您的开发环境已安装JDK 17。
- 编译DLL项目时，需安装Visual Studio，并确保编译环境配置正确。
- 运行`build.py`脚本前，请确保已安装Python 3环境。

## 贡献

欢迎对本项目进行改进和扩展，如果您有任何建议或问题，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅`LICENSE`文件。

## 下载链接

[JavaFXSpringBoot2.7JDK17Launch4jInnoSetup实现JVMTI的Jar包加密H2数据](https://pan.quark.cn/s/e040c483e9be)