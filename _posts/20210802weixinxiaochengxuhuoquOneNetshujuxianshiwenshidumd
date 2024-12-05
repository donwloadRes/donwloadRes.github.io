---
layout: post
title: "微信小程序获取OneNet数据显示温湿度"
date:   2022-06-08
tags: [OneNet,温湿度,微信,数据,api]
comments: true
author: admin
---
# 微信小程序获取OneNet数据显示温湿度

## 项目简介

本项目详细介绍了如何通过微信小程序获取OneNet平台上的温湿度数据，并展示了界面设计和代码实现过程。利用ApiPost测试MQTT API获取数据，并在小程序中展示最新的温湿度读数。同时提供了源码链接以及后续对小程序功能的扩展，包括控制灯的开关和数据定时刷新。

## 功能特点

1. **数据获取**：通过MQTT协议从OneNet平台获取温湿度数据。
2. **界面设计**：微信小程序界面设计，展示温湿度数据。
3. **代码实现**：提供详细的代码实现过程，方便开发者学习和参考。
4. **功能扩展**：支持控制灯的开关和数据定时刷新功能。

## 使用步骤

1. **OneNet平台配置**：
   - 设备通过MQTT协议连接到OneNet平台。
   - 获取产品的api-key和设备id。
   - 查询OneNet平台多协议接入文档，查看MQTT的API使用方法。

2. **微信小程序开发**：
   - 设计小程序界面，展示温湿度数据。
   - 使用wx.request获取数据，并在界面中展示。
   - 添加按钮点击事件，实现数据的实时获取和展示。

3. **ApiPost测试**：
   - 使用ApiPost测试是否能成功获取数据。

## 代码示例

以下是微信小程序中获取OneNet数据的代码示例：

```javascript
points: function(e) {
  var that = this;
  wx.request({
    url: 'http://api.heclouds.com/devices/xxxxxxxxxx/datapoints', // 设备ID
    header: {
      "api-key": "xxxxxxx" // 这里写你的api-key
    },
    data: {
      limit: 1
    },
    method: "GET",
    success: function(res) {
      that.setData({
        shidu: res.data.data.datastreams[0].datapoints[0].value, // 这里的shidu要跟wxml[[shidu]] 名字相同
        wendu: res.data.data.datastreams[1].datapoints[0].value
      });
    }
  });
}
```

## 后续扩展

1. **控制灯的开关**：在小程序中添加控制灯开关的功能。
2. **数据定时刷新**：实现数据的定时刷新，确保数据的实时性。

## 注意事项

- 确保微信小程序的合法域名设置正确。
- 根据实际需求调整代码中的设备ID和api-key。

## 贡献

欢迎开发者提出改进建议和贡献代码，共同完善本项目。

## 许可证

本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[微信小程序获取OneNet数据显示温湿度](https://pan.quark.cn/s/4a152fa67890)