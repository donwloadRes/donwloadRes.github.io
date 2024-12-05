---
layout: post
title: "STM32与ESP8266物联网项目"
date:   2022-03-18
tags: [OneNet,ESP8266,STM32,微控制器,OLED]
comments: true
author: admin
---
# STM32与ESP8266物联网项目

## 项目介绍

本项目基于STM32F103C8T6（或C6T6）微控制器，结合ESP8266模块，实现了温湿度、光照强度的采集与显示，并通过OneNet云平台进行数据上传和远程控制。具体功能包括：

- 使用DHT11传感器采集温湿度数据。
- 使用BH1750传感器采集光照强度数据。
- 在本地OLED显示屏上实时显示采集到的数据。
- 通过ESP8266模块将数据上传至OneNet云平台。
- 远程控制LED灯的状态和亮度（PWM调节）。

## 硬件需求

- STM32F103C8T6（或C6T6）微控制器
- ESP8266模块
- DHT11温湿度传感器
- BH1750光照强度传感器
- OLED显示屏
- LED灯
- 电阻、电容等基础电子元件

## 软件需求

- Keil uVision IDE
- OneNet云平台账号
- 相关库文件（如DHT11库、BH1750库、OLED库等）

## 项目结构

```
├── src
│   ├── main.c
│   ├── dht11.c
│   ├── bh1750.c
│   ├── oled.c
│   ├── esp8266.c
│   └── onenet.c
├── inc
│   ├── dht11.h
│   ├── bh1750.h
│   ├── oled.h
│   ├── esp8266.h
│   └── onenet.h
├── README.md
└── LICENSE
```

## 使用说明

1. **硬件连接**：按照电路图将各传感器和模块正确连接到STM32微控制器。
2. **软件配置**：在Keil uVision中导入项目文件，配置好相关库文件和编译选项。
3. **OneNet配置**：在OneNet云平台上创建相应的产品和设备，获取API Key和设备ID。
4. **代码修改**：在`onenet.c`文件中填入你的OneNet API Key和设备ID。
5. **编译下载**：编译项目并下载到STM32微控制器中。
6. **运行测试**：启动系统，观察OLED显示屏上的数据，并通过OneNet云平台进行远程控制测试。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 贡献

欢迎任何形式的贡献，包括但不限于代码优化、功能扩展、文档改进等。请通过提交Issue或Pull Request的方式参与贡献。

## 联系我们

如有任何问题或建议，请通过以下方式联系我们：

- 邮箱：[your-email@example.com]
- GitHub Issue：[项目Issue页面](https://github.com/your-repo/issues)

感谢您的关注和支持！

## 下载链接

[STM32与ESP8266物联网项目](https://pan.quark.cn/s/d232a9e36a7a)