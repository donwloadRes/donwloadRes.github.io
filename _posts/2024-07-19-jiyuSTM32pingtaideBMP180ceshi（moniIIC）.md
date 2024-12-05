---
layout: post
title: "基于STM32平台的BMP180测试（模拟IIC）"
date:   2020-05-05
tags: [IIC,BMP180,Byte,uint8,Send]
comments: true
author: admin
---
# 基于STM32平台的BMP180测试（模拟IIC）

## 简介
本资源文件详细记录了基于STM32平台使用模拟IIC通信协议测试BMP180传感器的过程。内容包括测试描述、硬件准备、数据手册解读、测试代码展示、遇到的问题及解决方法，最终得出稳定可靠的测试结果。

## 测试描述
使用模拟IIC，从BMP180中获取ID号、温度值、气压值以及计算海拔高度。

## 测试准备
- **硬件平台**：原子战舰V3开发板
- **测试工具**：逻辑分析仪、串口调试工具

## 数据手册解读
1. 多个字节的读取时序图，BMP180芯片的地址+写信号是0xEE，地址+读信号为0xEF。
2. 测试时默认使用低功耗模式，OSS的值需注意，因为后期的计算需要这个，并且读取UT值时也要做对应的处理。
3. 手册里给出的利用BMP180里的参数计算气压和温度的流程图，特别注意流程里的OSS。

## 测试代码
由于本工程是直接使用原子战舰的标准例程-库函数版本\实验23 IIC实验源码改过来的，所以模拟IIC部分使用的原子这块的代码，BMP180部分由本人编写。

### BMP180 C代码片
```c
#include "bmp180.h"
#include "delay.h"
#include "math.h"

//存储BMP180数据的结构
_bmp180 bmp180;

//BMP180初始化
//对使用的IIC端口进行初始化
void BMP_Init(void) {
    IIC_Init();
}

//写一个数据到BMP180
void BMP_WriteOneByte(uint8_t WriteAddr, uint8_t DataToWrite) {
    IIC_Start();
    IIC_Send_Byte(0xEE);
    IIC_Wait_Ack();
    IIC_Send_Byte(WriteAddr);
    IIC_Wait_Ack();
    IIC_Send_Byte(DataToWrite);
    IIC_Wait_Ack();
    IIC_Stop();
}

//从BMP180读一个字节数据
uint8_t BMP_ReadOneByte(uint8_t ReadAddr) {
    uint8_t data = 0;
    IIC_Start();
    IIC_Send_Byte(0xEE);
    IIC_Wait_Ack();
    IIC_Send_Byte(ReadAddr);
    IIC_Wait_Ack();
    IIC_Start();
    IIC_Send_Byte(0xEF);
    IIC_Wait_Ack();
    data = IIC_Read_Byte(1);
    IIC_Stop();
    return data;
}

//从BMP180读一个16位的数据
short BMP_ReadTwoByte(uint8_t ReadAddr) {
    // 代码省略
}
```

## 遇到的问题及解决方法
在测试过程中，可能会遇到数据读取不准确或通信不稳定的问题。通过仔细检查硬件连接、确认IIC通信时序、以及正确配置BMP180的初始化参数，可以有效解决这些问题。

## 结论
通过本资源文件提供的测试代码和详细步骤，用户可以在STM32平台上成功测试BMP180传感器，获取准确的温度、气压和海拔数据。

## 下载链接

[基于STM32平台的BMP180测试模拟IIC分享](https://pan.quark.cn/s/6b4b840fbc4b)