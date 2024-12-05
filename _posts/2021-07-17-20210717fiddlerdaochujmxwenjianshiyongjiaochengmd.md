---
layout: post
title: "fiddler导出jmx文件使用教程"
date:   2021-03-18
tags: [fiddler,jmx,导出,JMeter,测试]
comments: true
author: admin
---
# fiddler导出jmx文件使用教程

欢迎来到fiddler导出jmx文件使用指南。本教程旨在帮助您学会如何有效地使用fiddler来捕获网络会话，并将其导出为JMX格式，以便于在Apache JMeter中复用这些会话进行性能测试。适用于那些需要从真实用户交互中快速创建负载测试场景的测试工程师和开发者。

## 快速入门

### **前置条件**
- 确保您的fiddler版本在4.6.2以上。
- 安装最新或兼容版本的JMeter（建议3.0及以上版本）。
  
### **安装fiddler插件**
1. **下载插件**: 从指定资源或分享链接获取`JmeterExporter.dll`与相关JavaScript文件(`CustomRules.js`)。
2. **放置插件**: 将`JmeterExporter.dll`放入fiddler的`ImportExport`目录，同时将`CustomRules.js`置于相应脚本目录。
3. **重启fiddler**以激活插件。

### **捕获与导出**
1. **配置fiddler**: 设置过滤规则，专注于需要录制的特定网站或请求类型。
2. **开始抓包**: 进行所需网站的操作以捕获会话。
3. **导出会话**: 抓包完成后，在fiddler中选择`File` -> `Export Sessions`，选择`All Sessions`或特定会话，保存为`.jmx`格式。

### **在JMeter中使用**
1. **导入jmx文件**: 打开JMeter，将刚刚导出的.jmx文件拖拽到测试计划中。
2. **调整与完善**: 根据需要调整请求详情，如修改服务器地址或加入缺失的配置。
3. **执行测试**: 完成上述步骤后，您可以运行测试，观察是否符合预期。

## 注意事项
- 在旧版本的fiddler或JMeter上可能遇到兼容性问题，请确保软件版本与插件匹配。
- 导出后的JMX文件可能需要一定的手动调整才能完美适配不同的测试环境。
- 对于特定的网页或应用，可能还需要处理验证码、动态令牌等安全措施。

通过跟随上述步骤，您将能够高效地利用fiddler的强大功能，结合JMeter的强大测试能力，为您的应用构建可靠的性能测试套件。祝您测试顺利！

## 下载链接

[fiddler导出jmx文件使用教程分享](https://pan.quark.cn/s/2e54fca5b783)