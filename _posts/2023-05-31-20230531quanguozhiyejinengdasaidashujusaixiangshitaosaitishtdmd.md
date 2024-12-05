---
layout: post
title: "全国职业技能大赛大数据赛项十套赛题（shtd）"
date:   2023-12-22
tags: [info,user,Hive,ods,分区]
comments: true
author: admin
---
# 全国职业技能大赛大数据赛项十套赛题（shtd）

## 项目描述

本项目提供了一个使用Scala编写的Spark工程代码，用于将MySQL数据库`shtd_store`中的表`user_info`、`sku_info`、`base_province`、`base_region`、`order_info`、`order_detail`的增量数据抽取到Hive的`ods`库中对应的表中。具体任务如下：

1. **增量抽取数据**：从`shtd_store`库中抽取`user_info`表的增量数据到Hive的`ods`库中表`user_info`。根据`ods.user_info`表中的`operate_time`或`create_time`作为增量字段（即MySQL中每条数据取这两个时间中较大的那个时间作为增量字段去和`ods`里的这两个字段中较大的时间进行比较），只将新增的数据抽入，字段名称、类型不变。

2. **添加静态分区**：同时添加静态分区，分区字段类型为String，且值为当前比赛日的前一天日期（分区字段格式为`yyyyMMdd`）。

3. **验证分区**：使用Hive CLI执行`show partitions ods.user_info`命令，将结果截图粘贴至对应报告中。

## 使用说明

1. **环境要求**：
   - Scala
   - Apache Spark
   - MySQL
   - Hive

2. **配置文件**：
   - 确保在项目中配置好MySQL和Hive的连接信息。

3. **运行步骤**：
   - 克隆本仓库到本地。
   - 配置好相关环境变量和连接信息。
   - 运行Scala编写的Spark工程代码。
   - 使用Hive CLI执行`show partitions ods.user_info`命令，验证分区结果。

## 贡献

欢迎任何形式的贡献，包括但不限于代码优化、文档改进、问题反馈等。请通过提交Issue或Pull Request来参与本项目的贡献。

## 许可证

本项目采用[MIT许可证](LICENSE)。

## 联系方式

如有任何问题或建议，请通过以下方式联系：

- 邮箱：[your-email@example.com]
- GitHub Issue：[链接](https://github.com/your-repo/issues)

---

感谢您的关注和支持！

## 下载链接

[全国职业技能大赛大数据赛项十套赛题shtd](https://pan.quark.cn/s/c4597ca77b8c)