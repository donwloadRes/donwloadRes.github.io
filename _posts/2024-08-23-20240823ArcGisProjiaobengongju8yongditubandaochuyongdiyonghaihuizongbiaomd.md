---
layout: post
title: "ArcGisPro脚本工具8用地图斑导出用地用海汇总表"
date:   2021-08-23
tags: [汇总表,Excel,------,...,工具]
comments: true
author: admin
---
# ArcGisPro脚本工具【8】——用地图斑导出用地用海汇总表

## 简介

本资源文件提供了一个使用Arcpy编写的脚本工具，该工具在ArcGISPro 2.8中用于汇总统计地图数据并生成Excel指标表。特别适用于处理规划用地和三调数据。工具包含多个嵌套小工具，尽管代码结构复杂，但能有效导出汇总信息。

## 功能特点

- **汇总统计**：在ArcGIS中汇总统计地图数据。
- **生成指标表**：生成包含大类、中类、小类3级分类的指标表，可自选分类级别。
- **导出Excel表格**：最终导出Excel表格，方便数据分析和报告生成。

## 使用说明

1. **输入要素类**：输入要素，如三调、规划用地等。
2. **输入地类编码**：输入【地类编码】的字段。
3. **输出汇总表位置**：指定生成的Excel文件的存放位置。
4. **汇总表类型**：选择生成汇总表的类型，可以多选。

## 注意事项

- 输入数据的准确性对结果有重要影响，使用前请确保数据无拓扑错误、字段值正确、不存在空格等问题。
- 工具脚本较为复杂，可能存在BUG，使用过程中如发现问题，请先检查数据准确性。

## 结果展示

生成的Excel文件内容如下：

| 大类 | 中类 | 小类 | 面积 | 备注 |
|------|------|------|------|------|
| ...  | ...  | ...  | ...  | ...  |

## 下载地址

请在下载仓库中获取该工具的下载链接。

---

**版权声明**：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[ArcGisPro脚本工具8用地图斑导出用地用海汇总表](https://pan.quark.cn/s/b73e44a76e2f)