---
layout: post
title: "ESP32学习笔记（49）——RFID RC522使用"
date:   2023-02-07
tags: [ESP32,mfrc522,RC522,RFID,Serial]
comments: true
author: admin
---
# ESP32学习笔记（49）——RFID RC522使用

欢迎来到第49篇ESP32学习笔记，本篇我们将深入探索如何在ESP32项目中集成并使用RFID RC522模块。RFID技术广泛应用于物品追踪、门禁控制等领域，而RC522是一款常用的低成本RFID读写器芯片，非常适合DIY爱好者和初学者进行实验和小型项目开发。

## 硬件准备

确保你有以下硬件设备：
- ESP32 开发板
- RFID RC522模块
- 杜邦线若干

## 软件环境设置

1. 使用Arduino IDE作为开发环境。
2. 安装ESP32相关的板卡管理器及库。
3. 需要添加RFID库到你的Arduino库中，可以通过库管理器搜索“MFRC522”并安装。

## 连接指南

- **RC522与ESP32的连接**：
  - SDA（MISO）连接至ESP32的2号引脚。
  - SCK连接至18号引脚。
  - MOSI连接至23号引脚。
  - RST连接至GPIO15。
  - SPI SS（即Slave Select），根据需要可以自由选择，这里假设使用5号引脚。

## 示例代码解读

在编写代码前，务必理解基本的SPI通信原理。以下是一个简单的启动RC522并读取卡号的示例框架：

```cpp
#include <SPI.h>
#include <MFRC522.h>

#define SS_PIN 5
#define RST_PIN 15
MFRC522 mfrc522(SS_PIN, RST_PIN);

void setup() {
  Serial.begin(9600);
  SPI.begin();
  mfrc522.PCD_Init(); // 初始化RC522
  Serial.println("RC522初始化成功");
}

void loop() {
  // 检测是否有卡靠近
  if (mfrc522.PICC_IsNewCardPresent()) {
    if (mfrc522.PICC_ReadCardSerial()) {
      Serial.print("卡片UID: ");
      String uidStr = "";
      for (byte i = 0; i < mfrc522.uid.size; i++) {
        uidStr += String(mfrc522.uid.uidByte[i] < 0x10 ? "0" : "") + String(mfrc522.uid.uidByte[i], HEX);
        Serial.print(mfrc522.uid.uidByte[i] < 0x10 ? "0" : "");
        Serial.print(mfrc522.uid.uidByte[i], HEX);
        if (i != mfrc522.uid.size - 1) Serial.print(":");
      }
      Serial.println();
    }
  }
  delay(500); // 延时等待下一张卡
}
```

## 实践与调试

- 确保电源稳定，模块间连接正确无误。
- 利用串口监视器查看输出，了解交互流程。
- 调整天线位置以获得最佳读取距离。

完成上述步骤后，你就能够开始利用ESP32和RFID RC522进行创意项目开发了。不断实践，你会更深入地掌握无线识别技术的精髓。祝你在物联网的世界里探索无限可能！

---

请参考详细教程 [ESP32学习笔记详情页](https://blog.csdn.net/qq_36347513/article/details/125045917)，进一步加深理解和应用知识。

## 下载链接

[ESP32学习笔记49RFIDRC522使用](https://pan.quark.cn/s/2144bbd0e683)