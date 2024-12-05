---
layout: post
title: "VB.NET水晶报表Crystal Reports学习资源"
date:   2021-01-22
tags: [报表,安装,Dim,rt,rtUserNameValues]
comments: true
author: admin
---
# VB.NET水晶报表Crystal Reports学习资源

本资源文件提供了关于VB.NET中使用水晶报表（Crystal Reports）的全面学习资料，包括开发环境的安装、程序示例、报表示例以及客户端运行环境的配置。

## 内容概述

### 1. 开发环境安装
- **开发工具**：Visual Studio 2017
- **开发包**：CRforVS13SP25 (包含CRRuntime_64bit_13_0_25.msi + CrystalReportsForVisualStudio.msi)

### 2. 报表开发
- **CrystalReportViewer控件使用**：报表界面的基本设置和数据显示。
- **Rpt报表设计**：使用CrystalReport设计报表，示例使用CrystalReport9。

### 3. 客户端运行环境
- **提示CLR20r3错误**：未安装Crystal Reports运行环境，可下载对应版本Runtime安装。
- **运行库缺失**：Windows常用运行库缺失，需要下载并安装相关库。

## 使用说明

1. **开发环境安装**：
   - 下载并安装Visual Studio 2017。
   - 下载CRforVS13SP25开发包并安装。

2. **报表开发**：
   - 使用CrystalReportViewer控件进行报表界面的基本设置。
   - 使用CrystalReport设计软件进行报表设计。

3. **客户端运行环境**：
   - 安装水晶报表Crystal Reports运行环境CRRuntime13_0_25。
   - 安装Windows常用运行库以避免运行环境安装错误。

## 示例代码

```vb.net
Dim rt As New ReportDocument
rt.Load("你的文件目录\XXX.rpt")
rt.SetDatabaseLogon("sa", "sa")

Dim rtFieldDefinitions As ParameterFieldDefinitions
Dim rtUserName As ParameterFieldDefinition
Dim rtUserNameValues As New ParameterValues
Dim rtUserNameDiscreteValue As New ParameterDiscreteValue
rtUserNameDiscreteValue.Value = TextBox1.Text

rtFieldDefinitions = rt.DataDefinition.ParameterFields
rtUserName = rtFieldDefinitions.Item("UserName")
rtUserNameValues = rtUserName.CurrentValues
rtUserNameValues.Clear()
rtUserNameValues.Add(rtUserNameDiscreteValue)
rtUserName.ApplyCurrentValues(rtUserNameValues)

CrystalReportViewer1.ReportSource = rt
CrystalReportViewer1.ShowLogo = False
CrystalReportViewer1.Refresh()
```

## 注意事项

- 在使用自带的水晶报表时，请确保已注册，否则只能使用30次。
- 客户端程序需要安装CRRuntime文件，如果出现dll failed to register错误，可能是由于Windows常用运行库缺失，需要安装相关库。

通过本资源文件，您将能够全面掌握VB.NET中水晶报表的开发和应用，提升您的报表设计和开发能力。

## 下载链接

[VB.NET水晶报表CrystalReports学习资源分享](https://pan.quark.cn/s/a28768d1adac)