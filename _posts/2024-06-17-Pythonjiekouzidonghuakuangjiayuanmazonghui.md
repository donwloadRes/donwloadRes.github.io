---
layout: post
title: "Python接口自动化框架源码总汇"
date:   2024-02-10
tags: [封装,Allure,接口,Python,pytest]
comments: true
author: admin
---
# Python接口自动化框架源码总汇

## 资源文件描述

本仓库提供了一个全面的接口自动化框架源码集合，涵盖了Python、Requests、Pytest、Allure、YAML、DDT（数据驱动测试）以及日志处理等多个技术栈。该框架旨在帮助开发者快速搭建和扩展接口自动化测试项目，提高测试效率和代码复用性。

## 分支介绍

### 分支1-4
- **pytest插件与运行规则**：详细介绍了如何使用pytest插件、运行规则以及参数配置，包括pytest.ini文件的配置、用例跳过、用例执行顺序、夹具（Fixture）等。
- **Fixture固件与Allure报告**：讲解了如何使用Fixture固件，包括contest.py的使用、断言以及Allure报告的生成。
- **Allure报告定制与数据驱动**：深入探讨了Allure报告的定制化以及如何使用Parametrize进行数据驱动测试。
- **requests模块详解**：详细介绍了requests模块的使用，包括Cookie和Session的关联处理。

### 分支5
- **接口统一请求封装**：提供了接口统一请求的封装方法，以及接口关联的封装技巧。

### 分支6
- **YAML测试用例封装**：介绍了如何规范YAML测试用例，并对接口关联封装和基础路径封装进行了改进。

### 分支7
- **热加载封装与断言封装**：讲解了热加载的封装方法以及断言的封装技巧。

### 分支8
- **数据类型处理与DDT封装**：详细介绍了数据类型处理的方法，并提供了DDT数据驱动的封装。

### 分支9
- **异常日志与BaseUrl封装**：讲解了异常日志的处理方法，并提供了BaseUrl的封装技巧。

## 使用说明

1. **克隆仓库**：使用`git clone`命令克隆本仓库到本地。
2. **切换分支**：根据需求切换到相应的分支，例如`git checkout branch-1`。
3. **安装依赖**：根据每个分支的`requirements.txt`文件安装所需的Python依赖包。
4. **运行测试**：使用pytest命令运行测试用例，并生成Allure报告。

## 贡献

欢迎开发者提交PR，共同完善和扩展该接口自动化框架。请确保提交的代码符合PEP8规范，并附上详细的修改说明。

## 许可证

本项目采用MIT许可证，详情请参阅`LICENSE`文件。

## 下载链接

[Python接口自动化框架源码总汇](https://pan.quark.cn/s/b0feb79b88c9)