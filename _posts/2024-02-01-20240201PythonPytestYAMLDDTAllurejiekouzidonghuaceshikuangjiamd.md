---
layout: post
title: "Python  Pytest  YAML  DDT  Allure 接口自动化测试框架"
date:   2023-03-20
tags: [测试,接口,测试用例,pytest,allure]
comments: true
author: admin
---
# Python + Pytest + YAML + DDT + Allure 接口自动化测试框架

## 简介

本仓库提供了一个基于 `Python`、`Pytest`、`YAML`、`DDT` 和 `Allure` 的接口自动化测试框架源码。该框架通过码尚的VIP课程学习，并结合公司项目进行升级改造，经过实际测试验证，功能稳定可靠。只需输入自己项目的接口用例数据，即可轻松实现自动化测试。

## 框架特点

- **Python**：简洁易读的编程语言，适合快速开发和测试。
- **Pytest**：强大的测试框架，支持多种测试场景和插件扩展。
- **YAML**：用于配置和数据驱动的测试用例，简化测试数据的维护。
- **DDT**：数据驱动测试，提高测试用例的复用性和可维护性。
- **Allure**：生成美观的测试报告，便于结果分析和问题定位。

## 使用说明

1. **环境准备**：
   - 安装Python 3.x
   - 安装必要的依赖库：`pip install pytest pytest-ddt allure-pytest`

2. **配置文件**：
   - 在 `config` 目录下，根据项目需求修改 `config.yaml` 文件，配置接口地址、请求头等信息。

3. **编写测试用例**：
   - 在 `test_cases` 目录下，使用 `YAML` 格式编写接口测试用例。
   - 使用 `DDT` 装饰器，将测试数据与测试方法绑定。

4. **执行测试**：
   - 在项目根目录下运行 `pytest` 命令，执行所有测试用例。
   - 使用 `allure` 生成测试报告：`pytest --alluredir=./allure-results`

5. **查看报告**：
   - 运行 `allure serve ./allure-results` 命令，查看生成的测试报告。

## 注意事项

- 请确保测试环境的稳定性，避免因环境问题导致测试失败。
- 定期更新框架依赖库，以获取最新的功能和修复。

## 致谢

感谢码尚的VIP课程，让我有机会学习和实践接口自动化测试。希望这个框架能够帮助到更多正在学习自动化测试的朋友，提升技术功底，共同进步！

## 联系我

如果你在使用过程中遇到任何问题，或有任何建议，欢迎通过GitHub Issues联系我。

## 下载链接

[PythonPytestYAMLDDTAllure接口自动化测试框架](https://pan.quark.cn/s/0f86b611360e)