---
layout: post
title: "C WinForm 简单三层框架源码共享"
date:   2021-10-06
tags: [NULL,COLLATE,Chinese,PRC,CI]
comments: true
author: admin
---
# C# WinForm 简单三层框架源码共享

## 项目简介

本项目提供了一个基于C# WinForm的简单三层框架源码，旨在帮助开发者快速搭建和扩展自己的系统。该框架采用经典的三层架构（DAL、BLL、UI）实现，适合习惯于Web开发的开发者快速上手。

## 框架特点

- **三层架构**：采用DAL（DBUtility）、BLL、UI三层架构，结构清晰，易于维护和扩展。
- **数据库配置**：数据库连接字符串配置在根目录的`DBCfg.xml`文件中，部分内容已加密，实际使用时只需配置一个数据库连接字符串即可。
- **方法丰富**：框架默认提供了多种常用方法，方便开发者快速进行二次开发。
- **数据库字符串修改窗体**：提供了一个方便的数据库字符串修改窗体，方便开发者进行配置。

## 使用说明

1. **下载源码**：从本仓库下载源码到本地。
2. **配置数据库**：在`DBCfg.xml`文件中配置数据库连接字符串。
3. **创建数据库表**：运行框架前，请先在数据库中创建所需的表。表结构如下：

```sql
CREATE TABLE [dbo].[Infos](
    [Iid] [int] IDENTITY(11) NOT NULL,
    [title] [varchar](255) COLLATE Chinese_PRC_CI_AS NULL,
    [details] [text] COLLATE Chinese_PRC_CI_AS NULL,
    [imgs] [varchar](5000) COLLATE Chinese_PRC_CI_AS NULL,
    [classify] [varchar](50) COLLATE Chinese_PRC_CI_AS NULL,
    [publiship] [varchar](30) COLLATE Chinese_PRC_CI_AS NULL,
    [publishman] [varchar](20) COLLATE Chinese_PRC_CI_AS NULL,
    [publishtime] [datetime] NULL,
    [isshow] [varchar](4) COLLATE Chinese_PRC_CI_AS NULL,
    [istop] [varchar](4) COLLATE Chinese_PRC_CI_AS NULL,
    [hits] [int] NULL,
    [notes] [varchar](255) COLLATE Chinese_PRC_CI_AS NULL,
    CONSTRAINT [PK_Infos] PRIMARY KEY CLUSTERED 
    (
        [Iid] ASC
    )WITH (PAD_INDEX  = OFF, STATISTICS_NORECOMPUTE  = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS  = ON, ALLOW_PAGE_LOCKS  = ON) ON [PRIMARY]
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
```

4. **运行项目**：配置完成后，直接运行项目即可。

## 注意事项

- 本框架仅供学习和参考使用，实际项目中请根据需求进行适当修改和扩展。
- 数据库字符串配置文件中的部分内容已加密，请勿随意修改。

## 贡献与反馈

如果您在使用过程中遇到问题或有任何建议，欢迎提交Issue或Pull Request。我们期待您的反馈和贡献！

## 下载链接

[CWinForm简单三层框架源码共享](https://pan.quark.cn/s/bf37b618da55)