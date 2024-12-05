---
layout: post
title: "MQTT.fx和MQTTX 链接ONENET物联网开发平台避坑细节干货"
date:   2023-10-31
tags: [ID,ONENET,设备,名称,MQTT]
comments: true
author: admin
---
# MQTT.fx和MQTTX 链接ONENET物联网开发平台避坑细节干货

本文详细介绍了如何使用MQTT.fx和MQTTX作为调试工具连接ONENET物联网平台，包括创建产品、设置参数、获取鉴权信息等步骤。文章特别提到了时间戳计算、设备名称和ClientID的匹配问题，并对比了ONENET与阿里云物联网平台的连接便捷性。

## 主要内容

### 1. 创建产品
- 点击开发者中心，创建账号并进行产品开发。
- 根据需求设置参数，选择联网方式。

### 2. 获取鉴权信息
- 设备名称、设备ID和access_key是ONENET的三大鉴权参数。
- access_key需要通过手机验证获取。

### 3. MQTT.fx连接配置
- 使用token计算工具生成TOKEN作为密码。
- 填写设备名称、产品ID等参数。
- 注意时间戳的计算，确保填写未来时间。

### 4. MQTTX连接配置
- 以设备名称mqtt_device为例进行连接配置。
- 确保设备名称与产品ID一致，避免连接错误。

### 5. 注意事项
- 设备名称与产品ID一致时，client ID为产品ID。
- 设备名称与产品ID不一致时，client ID和token中的res需填写设备名称/ID。

通过本文的详细步骤和注意事项，开发者可以顺利使用MQTT.fx和MQTTX连接ONENET物联网平台，避免常见错误。

## 下载链接

[MQTT.fx和MQTTX链接ONENET物联网开发平台避坑细节干货](https://pan.quark.cn/s/841aeb7ee3bb)