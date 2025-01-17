---
layout: post
title: "CC工具箱使用指南三调土地利用现状三大类面积汇总表"
date:   2020-09-22
tags: [面积,三调,汇总表,图层,工具]
comments: true
author: admin
---
# CC工具箱使用指南：三调土地利用现状三大类面积汇总表

## 简介
本资源文件提供了CC工具箱的使用指南，特别是针对“三调_土地利用现状三大类面积汇总表”的统计工具。该工具旨在帮助用户根据《TDT 1055-2019 第三次全国国土调查技术规程》的附表B1格式，生成土地利用现状一级分类面积汇总表。

## 工具参数介绍
1. **选择三调图层**：
   - 正常的三调图层自带了【DLMC、KCXS、ZLDWDM、ZLDWMC】字段，工具需要用到这些字段，请确保字段完整。

2. **选择分地块图层**：
   - 如果你想统计整个三调图层的面积，可以不填写此参数。如果只想统计局部范围内的面积，可以创建一个分地块图层，并在其中创建一个文本型字段作为统计表的表名。

3. **选择分地块名称字段**：
   - 即分地块图层中创建的用来标记统计表名的文本型字段。

4. **计算平差**：
   - 由于统计面积时需要保留小数位数，可能会导致总面积存在误差。勾选此选项可以平衡误差，使汇总的总面积符合用地范围的面积。

5. **面积类型**：
   - 可以选择汇总的面积类型，包括【投影面积或椭球面积】。

6. **面积单位**：
   - 可以选择汇总的面积单位，包括【平方米、公顷、平方公里、亩】。

7. **面积保留的小数位数**：
   - 可以选择汇总的面积数值的保留位数，范围为【1至6位】。

8. **输出Excel表格的路径**：
   - 设置一个输出路径，工具将在此路径下生成Excel表格。

9. **数据检查**：
   - 工具执行前可以进行数据检查，确保输入数据格式正确。

## 工具执行结果
工具正常执行后，会生成相应的统计结果。如果存在分地块，每个分地块的统计结果会生成对应的子表，子表名即为分地块的名称字段值。

## 使用说明
1. 下载并安装CC工具箱。
2. 按照上述参数介绍，设置好工具参数。
3. 执行工具，生成土地利用现状三大类面积汇总表。

## 注意事项
- 确保输入数据字段完整，避免因字段缺失导致工具无法正常运行。
- 在进行数据检查时，仔细核对检查结果，确保数据格式无误。

通过本工具，用户可以高效地生成土地利用现状三大类面积汇总表，满足国土调查的需求。

## 下载链接

[CC工具箱使用指南三调土地利用现状三大类面积汇总表](https://pan.quark.cn/s/1b72caf66b08)