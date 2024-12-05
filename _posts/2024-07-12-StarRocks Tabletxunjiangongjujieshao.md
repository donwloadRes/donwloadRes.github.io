---
layout: post
title: "StarRocks Tablet巡检工具介绍"
date:   2024-03-27
tags: [StarRocks,工具,集群,Tablet,数据库]
comments: true
author: admin
---
# StarRocks Tablet巡检工具介绍

## 概述
本资源文件提供了一个用于StarRocks集群的Tablet巡检工具。该工具旨在帮助数据库管理员（DBA）评估OLAP数据表的分桶是否合理，并提供详细的统计信息，以便更好地管理和优化StarRocks集群。

## 工具用途
1. **统计和导出Tablet体积信息**：该工具可以统计和导出StarRocks集群中的Tablet体积信息，包括表大小、副本个数、表tablet体积的最大值、最小值、平均值以及标准差。
2. **数据倾斜检测**：通过统计信息，工具可以帮助用户定位是否存在数据倾斜问题。
3. **结果导出**：工具支持将统计结果导出为标准的CSV文件，方便用户使用Excel等工具进行进一步分析。

## 使用方法
1. **运行环境**：该工具使用Java语言编写，运行前请确保当前系统具备JAVA运行环境。
2. **命令行参数**：
   - `参数1`：配置文件路径及名称，默认为当前路径下的`config.properties`，默认情况下可以省略。
   - `参数2`：需要生成的csv文件路径及文件名，参数2不写时不会生成文件，只写文件名不写路径时默认在当前路径生成。当需要生成文件时，参数1不能省略，并且参数2需以`.csv`结尾。

## 配置文件说明
在`config.properties`中需提前配置StarRocks的集群信息，包括：
- `host`：集群中任意一个FE的IP和查询端口。
- `username`：StarRocks用户名。
- `password`：StarRocks密码。
- `database`：数据库名称，支持配置单个数据库或以英文逗号分割的多个数据库以及留空，当为空时将扫描所有数据库。
- `tablename`：表名称，当为空时将扫描数据库下所有表，配置多个表时需以英文逗号分隔。

## 示例
```bash
java -jar starrocks-tablet-tool.jar config.properties demo.csv
```

## 注意事项
- 该工具适用于StarRocks 2.4及以后版本。
- 建议将每个tablet的数据量控制在压缩前10G左右，以确保集群的性能和稳定性。

通过使用该工具，用户可以更有效地管理和优化StarRocks集群，提升数据处理效率和查询性能。

## 下载链接

[StarRocksTablet巡检工具介绍](https://pan.quark.cn/s/322448febf58)