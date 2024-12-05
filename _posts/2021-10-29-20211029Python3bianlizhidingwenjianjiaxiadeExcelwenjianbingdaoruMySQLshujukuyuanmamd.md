---
layout: post
title: "Python3 遍历指定文件夹下的Excel文件并导入MySQL数据库源码"
date:   2022-06-29
tags: [Excel,MySQL,数据库,文件夹,脚本]
comments: true
author: admin
---
# Python3 遍历指定文件夹下的Excel文件并导入MySQL数据库源码

## 简介

本资源文件提供了一个Python3脚本的源码，该脚本的功能是遍历指定文件夹下的所有Excel文件，并将其中的数据导入到MySQL数据库中。脚本支持读取Excel文件中的多个Sheet，并可以选择性地导入指定的Sheet数据。

## 功能描述

- **遍历文件夹**：脚本会遍历指定文件夹下的所有Excel文件（.xlsx 或 .xls 格式）。
- **读取Excel数据**：对于每个Excel文件，脚本会读取其中的多个Sheet，并可以选择性地导入指定的Sheet数据。
- **数据导入MySQL**：读取的数据将被导入到MySQL数据库中，支持自定义数据库连接信息和表结构。

## 环境要求

- Python 3.x
- 需要安装以下Python库：
  - `pandas`：用于读取Excel文件。
  - `mysql-connector-python`：用于连接和操作MySQL数据库。

## 使用说明

1. **安装依赖库**：
   ```bash
   pip install pandas mysql-connector-python
   ```

2. **配置数据库连接**：
   在脚本中配置MySQL数据库的连接信息，包括数据库地址、用户名、密码、数据库名称等。

3. **指定文件夹路径**：
   在脚本中指定需要遍历的文件夹路径。

4. **运行脚本**：
   运行Python脚本，脚本将自动遍历指定文件夹下的所有Excel文件，并将数据导入到MySQL数据库中。

## 注意事项

- 确保MySQL数据库已启动并可访问。
- 确保Excel文件格式正确，且Sheet名称符合预期。
- 如果Excel文件较大，可能需要调整Python的内存限制。

## 贡献

欢迎提交问题和改进建议，帮助完善此脚本。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[Python3遍历指定文件夹下的Excel文件并导入MySQL数据库源码分享](https://pan.quark.cn/s/4fc490871456)