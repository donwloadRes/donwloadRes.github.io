---
layout: post
title: "天气后报网爬虫及数据分析Python"
date:   2022-12-14
tags: [data,csv,爬虫,天气,文件]
comments: true
author: admin
---
# 天气后报网爬虫及数据分析（Python）

## 项目描述

本项目旨在从天气后报网（http://www.tianqihoubao.com）中爬取绵阳市某一年的历史天气信息，并对获取的数据进行分析。具体功能包括：

1. **数据爬取与存储**：从网站中爬取每天的最高气温、最低气温、天气状况、风向等信息，并将这些数据存储到名为“data.csv”的文件中。每行数据的格式为“日期，最高温，最低温，天气，风向”。

2. **数据处理**：在“data.csv”文件中增加“平均温度”一列，计算公式为：平均温度 = （最高温 + 最低温）/ 2。

3. **数据统计**：统计并输出“data.csv”文件中平均气温在20-26°的总天数。

4. **天气类型统计与可视化**：统计这一年中多云、晴天、雨天、阴天的天数（阴/多云可以当作阴天），并使用Matplotlib库将各类天气的天数制作成饼图并保存。

5. **月度气温统计**：统计并输出这一年中每个月的最高气温和最低气温。

6. **季度气温走势图**：选取这一年中的某个季度，使用Matplotlib库绘制并保存最高温和最低温的走势图。

## 使用说明

1. **环境准备**：确保已安装Python 3.x，并安装所需的依赖库，如`requests`、`BeautifulSoup`、`pandas`、`matplotlib`等。

2. **运行爬虫**：运行爬虫脚本，从天气后报网爬取数据并存储到“data.csv”文件中。

3. **数据处理与分析**：运行数据处理脚本，对“data.csv”文件中的数据进行处理和分析，生成统计结果和可视化图表。

4. **查看结果**：查看生成的“data.csv”文件、统计结果输出以及保存的图表文件。

## 注意事项

- 爬虫脚本需遵守网站的Robots协议，避免对目标网站造成过大负担。
- 数据分析结果仅供参考，具体分析标准可根据实际需求进行调整。

## 贡献

欢迎对本项目提出改进建议或贡献代码。请通过GitHub的Pull Request功能提交您的修改。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[天气后报网爬虫及数据分析Python](https://pan.quark.cn/s/bc6dd8318bba)