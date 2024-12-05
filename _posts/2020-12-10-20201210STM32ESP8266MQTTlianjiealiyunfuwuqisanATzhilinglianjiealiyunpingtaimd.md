---
layout: post
title: "STM32ESP8266MQTT连接阿里云服务器三AT指令连接阿里云平台"
date:   2020-02-24
tags: [指令,MQTT,连接,阿里,ID]
comments: true
author: admin
---
# STM32+ESP8266+MQTT连接阿里云服务器（三、AT指令连接阿里云平台）

## 简介

本资源文件详细介绍了如何使用STM32微控制器通过AT指令连接阿里云物联网平台。通过本教程，您将学习到如何配置设备证书、设置AT指令、同步SNTP时间、连接WiFi、配置MQTT用户属性、设置客户端ID、连接MQTT Broker、订阅与发布主题等步骤。通过这些操作，STM32设备能够成功上线并收发数据，实现远程监控与调试。

## 主要内容

### 准备工作

1. **查看设备证书**：为后续连接做准备。
2. **利用阿里云配置工具生成设备信息及客户端ID**：通过阿里云物联平台配置工具生成客户端ID、用户名和密码。

### AT指令连接阿里云平台

1. **重启设备**：使用`AT+RST`指令重启设备。
2. **设置AP+Station模式**：使用`AT+CWMODE=3`指令设置AP+Station模式。
3. **开启SNTP服务器**：使用`AT+CIPSNTPCFG=1,8,"ntp1.aliyun.com"`指令开启SNTP服务器，设置时域为8，SNTP服务器为阿里云域名。
4. **连接WiFi**：使用`AT+CWJAP="YCF","ycf88888888"`指令连接WiFi。
5. **配置MQTT用户属性**：使用`AT+MQTTUSERCFG=0,1,"NULL","C6T6&gavk88e3djY","64678A30225AB875CA6A6C323DAA575A3B283AB7",0,0,""`指令配置MQTT用户属性。
6. **配置MQTT客户端ID**：使用`AT+MQTTCLIENTID=0,"112233|securemode=3,signmethod=hmacsha1,timestamp=456|"`指令配置MQTT客户端ID。
7. **连接MQTT Broker**：使用`AT+MQTTCONN=0,"gavk88e3djY.iot-as-mqtt.cn-shanghai.aliyuncs.com",1883,1`指令连接MQTT Broker。
8. **订阅主题**：使用`AT+MQTTSUB=0,"/sys/gavk88e3djY/C6T6/thing/service/property/set",1`指令订阅主题。
9. **发布消息**：使用`AT+MQTTPUB=0,"/sys/gavk88e3djY/C6T6/thing/event/property/post","test",1,0`指令发布消息。

## 使用方法

1. **下载资源文件**：从本仓库下载资源文件。
2. **配置设备证书**：根据阿里云平台生成的设备证书进行配置。
3. **编写AT指令**：根据上述步骤编写AT指令，并通过串口发送给ESP8266模块。
4. **验证连接**：在阿里云管理平台查看设备是否在线，并通过串口调试助手打印订阅的消息数据。

## 注意事项

- 请确保所有AT指令中的参数与您创建的产品信息一致。
- 在发送AT指令时，请确保串口通信正常，避免数据丢失或错误。

通过本教程，您将能够成功实现STM32与阿里云物联网平台的连接，实现远程监控与数据传输。

## 下载链接

[STM32ESP8266MQTT连接阿里云服务器三AT指令连接阿里云平台](https://pan.quark.cn/s/dfe565291bd7)