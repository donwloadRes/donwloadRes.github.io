---
layout: post
title: "ESP8266实现手机App控制例程"
date:   2020-05-07
tags: [ESP8266,WiFi,App,创建,例程]
comments: true
author: admin
---
# ESP8266实现手机App控制例程

## 资源描述

本资源文件提供了一个基于ESP8266模块的例程，用于实现通过手机App控制的功能。通过该例程，您可以轻松创建一个WiFi热点，并使用手机App与之通信，实现远程控制。

## 主要功能

### 函数名：ESP8266_BuildAP

**描述**：该函数用于创建一个WiFi热点，使ESP8266模块能够作为WiFi接入点。

**输入参数**：
- `pSSID`：WiFi名称字符串。
- `pPassWord`：WiFi密码字符串。
- `enunPsdMode`：WiFi加密方式代号字符串。

**返回值**：
- `1`：创建成功。
- `0`：创建失败。

**调用方式**：该函数可以被外部调用，用于创建WiFi热点。

**示例代码**：
```c
bool ESP8266_BuildAP(char *pSSID, char *pPassWord, ENUM_AP_PsdMode_TypeDef enunPsdMode) {
    char cCmd[120];
    sprintf(cCmd, "AT+CWSAP=%s,%s,1,%d", pSSID, pPassWord, enunPsdMode);
    return ESP8266_Cmd(cCmd, "OK", 0, 1000);
}
```

## 使用说明

1. **配置WiFi热点**：
   - 调用`ESP8266_BuildAP`函数，传入WiFi名称、密码和加密方式，创建WiFi热点。
   - 确保ESP8266模块已正确连接并初始化。

2. **手机App连接**：
   - 使用手机App连接到ESP8266创建的WiFi热点。
   - 通过App发送控制指令，实现远程控制功能。

3. **调试与测试**：
   - 在调试过程中，可以通过串口监视器查看ESP8266模块的输出信息，确保WiFi热点创建成功。
   - 测试手机App与ESP8266的通信是否正常。

## 注意事项

- 确保ESP8266模块的固件版本支持WiFi热点创建功能。
- 在配置WiFi热点时，注意选择合适的加密方式，确保网络安全。
- 如果创建失败，请检查输入参数是否正确，并确保ESP8266模块工作正常。

## 适用场景

该例程适用于需要通过手机App远程控制ESP8266模块的场景，如智能家居、物联网设备控制等。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交Issue或Pull Request。我们期待您的反馈与贡献！

## 下载链接

[ESP8266实现手机App控制例程](https://pan.quark.cn/s/77e5ac9e6f96)