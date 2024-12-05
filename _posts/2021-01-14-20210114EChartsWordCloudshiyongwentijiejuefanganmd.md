---
layout: post
title: "ECharts WordCloud 使用问题解决方案"
date:   2021-08-27
tags: [echarts,ECharts,wordCloud,wordcloud,插件]
comments: true
author: admin
---
# ECharts WordCloud 使用问题解决方案

## 简介

本资源文件旨在解决在使用 ECharts 的 WordCloud 功能时遇到的常见问题：`series.wordCloud not exists, load it first`。该问题通常是由于 ECharts 版本更新后，WordCloud 功能不再默认包含在主包中，需要单独引入所致。

## 问题描述

在使用 ECharts 绘制词云图时，可能会遇到以下错误提示：

```
series.wordCloud not exists, load it first
```

此错误表明 ECharts 无法识别 `wordCloud` 系列类型，原因是 ECharts 2.0 版本之后不再默认支持 WordCloud，需要单独引入相关插件。

## 解决方案

### 1. 单独引入 WordCloud 插件

为了解决上述问题，您需要单独引入 `echarts-wordcloud` 插件。可以通过以下步骤进行操作：

1. **下载插件文件**：
   - 您可以从本仓库中下载 `echarts-wordcloud.min.js` 文件。

2. **引入插件**：
   - 在您的项目中引入 `echarts-wordcloud.min.js` 文件。例如：
     ```javascript
     import wordCloud from './path/to/echarts-wordcloud.min.js';
     ```

3. **使用 WordCloud 系列**：
   - 在您的 ECharts 配置中，使用 `wordCloud` 系列类型：
     ```javascript
     option = {
       series: [
         {
           type: 'wordCloud',
           // 其他配置项
         }
       ]
     };
     ```

### 2. 确保 ECharts 版本兼容

请确保您使用的 ECharts 版本与 `echarts-wordcloud` 插件版本兼容。通常情况下，`echarts-wordcloud` 2.x 版本适用于 ECharts 5.x 版本。

## 示例代码

以下是一个简单的示例代码，展示如何使用 `echarts-wordcloud` 插件绘制词云图：

```javascript
import * as echarts from 'echarts';
import wordCloud from './path/to/echarts-wordcloud.min.js';

// 初始化 ECharts 实例
var myChart = echarts.init(document.getElementById('main'));

// 配置项
var option = {
  series: [
    {
      type: 'wordCloud',
      data: [
        { name: 'ECharts', value: 100 },
        { name: 'WordCloud', value: 80 },
        // 更多数据项
      ]
    }
  ]
};

// 设置配置项
myChart.setOption(option);
```

## 总结

通过单独引入 `echarts-wordcloud` 插件，您可以轻松解决 `series.wordCloud not exists, load it first` 错误，并成功绘制词云图。希望本资源文件对您有所帮助！

---

**注意**：本资源文件仅供学习和参考使用，具体实现请根据您的项目需求进行调整。

## 下载链接

[EChartsWordCloud使用问题解决方案分享](https://pan.quark.cn/s/13e5cc8c4fd3)