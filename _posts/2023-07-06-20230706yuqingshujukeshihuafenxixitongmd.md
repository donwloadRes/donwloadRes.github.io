---
layout: post
title: "舆情数据可视化分析系统"
date:   2021-10-05
tags: [舆情,抓取,数据,可视化,分析]
comments: true
author: admin
---
# 舆情数据可视化分析系统

## 项目简介

本项目是一个基于Python、Flask Web框架、MySQL数据库、SnowNLP自然语言处理库以及ECharts数据可视化库构建的舆情数据可视化分析系统。该系统主要用于分析和可视化突发公共卫生事件的舆情数据，通过从微博热搜和抖音热点中抓取数据，并根据特定关键词进行筛选和分析，最终生成不同阶段的舆情分析图表。

## 技术框架

- **Python**：作为主要编程语言，负责数据处理、爬虫、自然语言处理等功能。
- **Flask Web**：用于搭建Web应用，提供用户界面和数据展示。
- **MySQL**：作为数据库，存储抓取的舆情数据。
- **SnowNLP**：用于情感分析，帮助判断舆情数据的情感倾向。
- **ECharts**：用于数据可视化，生成折线图、云词图等图表。

## 功能模块

### 1. 爬虫模块
- **数据抓取**：系统启动后，会开启一个线程定时从微博热搜和抖音热点中抓取数据。
- **数据筛选**：抓取的数据会根据标题中的特定字符（如“突发”、“疫情”、“大白”、“口罩”等）进行筛选，只有符合条件的数据才会被写入数据库。

### 2. 登录模块
- **用户登录**：提供用户登录功能，确保系统的安全性。

### 3. 可视化模块
- **折线图**：展示不同阶段的舆情分析结果，帮助用户直观了解舆情变化趋势。
- **云词图**：通过词云图展示舆情数据中的关键词分布，帮助用户快速了解舆情热点。

### 4. 分析模块
- **情感分析**：使用SnowNLP对抓取的数据进行情感分析，判断舆情数据的情感倾向。
- **不同阶段分析**：根据抓取的数据，生成不同阶段的舆情分析图表，帮助用户深入了解舆情发展过程。

### 5. 子模块
- **折线图**：根据每天抓取的数据绘制折线图，分析每一天的舆情值。
- **云词图**：生成云词图，展示不同阶段的舆情关键词分布。

## 注意事项

- 在爬虫抓取数据后，系统会根据标题中的特定字符进行筛选，只有符合条件的数据才会被写入数据库。
- 系统使用高版本的Python 3.9.6，并使用高版本的Jieba分词库，确保舆情分析的准确性。

## 使用说明

1. **启动系统**：运行Flask Web应用，启动舆情数据可视化分析系统。
2. **数据抓取**：系统会自动开启线程，定时从微博热搜和抖音热点中抓取数据。
3. **数据分析**：抓取的数据会经过筛选和情感分析，生成不同阶段的舆情分析图表。
4. **可视化展示**：用户可以通过Web界面查看生成的折线图和云词图，了解舆情变化和热点分布。

## 未来展望

本项目将持续优化和扩展，增加更多数据源和分析功能，提升舆情分析的准确性和可视化效果。欢迎开发者参与贡献，共同完善这一舆情数据可视化分析系统。

## 下载链接

[舆情数据可视化分析系统](https://pan.quark.cn/s/bedc84c52c66)