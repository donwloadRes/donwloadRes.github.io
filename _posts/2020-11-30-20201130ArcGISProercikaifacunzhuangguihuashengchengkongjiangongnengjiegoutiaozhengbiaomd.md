---
layout: post
title: "ArcGIS Pro二次开发：村庄规划生成空间功能结构调整表"
date:   2024-05-31
tags: [规划,用地,工具,功能,村庄]
comments: true
author: admin
---
# ArcGIS Pro二次开发：村庄规划生成空间功能结构调整表

本资源文件提供了一个用于ArcGIS Pro二次开发的工具，该工具主要用于村庄规划中的空间功能结构调整表的生成。通过该工具，用户可以方便地汇总村庄的现状用地和规划用地，并生成相应的Excel表格，以便进行空间功能结构的调整和分析。

## 功能概述

该工具的主要功能包括：
1. **选择图层**：用户可以选择现状用地和规划用地图层。
2. **定义用地属性**：工具会根据用户选择的图层，自动提取用地属性。
3. **映射功能代码**：将用地属性映射为功能代码，便于后续统计和分析。
4. **统计面积**：计算并汇总各用地的面积。
5. **生成Excel表格**：将统计结果导出为Excel表格，方便用户进行进一步的数据处理和分析。

## 使用步骤

1. **选择图层**：在ArcGIS Pro中加载现状用地和规划用地图层。
2. **运行工具**：点击工具栏中的“汇总村庄空间功能结构调整表”工具。
3. **设置输出路径**：选择保存生成的Excel文件的路径。
4. **执行**：点击“执行”按钮，工具将自动生成并保存空间功能结构调整表。

## 注意事项

- 输入的现状用地图斑需要包含两个字段：`JQDLBM`（基期地类编码）和`CZCSXM`（三调用地的城镇村属性）。
- 输入的规划用地图斑需要包含两个字段：`GHDLBM`（规划地类编码）和`SSBJLX`（规划用地的城镇村属性）。

## 适用场景

该工具适用于国土空间规划、村庄规划等领域，特别是在需要进行空间功能结构调整和分析的场景中，能够大大提高工作效率。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有任何建议，欢迎通过GitHub提交Issue或Pull Request。我们非常欢迎您的贡献和反馈，以帮助我们不断改进和完善该工具。

---

通过使用本工具，您可以更加高效地完成村庄规划中的空间功能结构调整工作，提升规划工作的质量和效率。

## 下载链接

[ArcGISPro二次开发村庄规划生成空间功能结构调整表](https://pan.quark.cn/s/1698fa224525)