---
layout: post
title: "MCGS串口驱动说明文档"
date:   2021-07-16
tags: [DIM,串口,MCGS,INTEGER,发送]
comments: true
author: admin
---
# MCGS串口驱动说明文档

MCGS（Monitor Control And Graphics Sheet）昆仑通态是一款广泛应用于工业自动化领域的组态软件，支持多种硬件设备的通讯。本文档旨在详细介绍如何在MCGS系统中实现串口通信功能，特别是通过脚本来控制串口通讯，适用于需要通过编程方式进行数据收发的应用场景。

## 引言

在工业控制系统中，触摸屏作为人机界面(HMI)，通常需要与PLC、传感器等设备通过串口进行数据交换。MCGS提供的串口驱动脚本，使得开发人员能够灵活地编写指令，实现设备间的高效通信。

## 核心脚本示例

以下是一段基础的MCGS串口通讯脚本代码示例，这段代码展示了如何准备并发送一个简单的串口命令，并接收回应，包含了HEXE协议格式的简单应用。

```vbnet
DIM strTmp as STRING   '临时字符变量
DIM strData as STRING   '用于构建命令或接收数据的字符串
DIM SendByteArr(0) as byte   '存放发送命令的字节数组
DIM RecByteArr(0) as byte   '存放接收数据的字节数组
DIM DataByteArr(0) as byte   '解析数据用的临时字节数组

DIM nReturn as INTEGER   '用于判断函数执行结果的标志
DIM nTmp as INTEGER   '开关型临时变量
DIM 数值数据 as SINGLE   '用于存储解析出的数值型数据
DIM 开关数据 as INTEGER   '用于存储解析出的开关型数据
DIM setFlag as SINGLE
DIM start as INTEGER
DIM j as INTEGER   '用来计算数据个数或循环计数

' CRC校验相关变量
DIM crc as SINGLE
DIM nCrc as INTEGER
DIM cstrTmp as STRING
DIM crcTmp as INTEGER
DIM csendTmp as STRING

'nIndex, nChlIndex等可以根据实际需求初始化，分别代表索引号和通道索引

' 示例中的发送逻辑：
IF i=0 THEN
    strSend = "*" + "!" + "$$$$$$$$$$$$$$$$$$$$" + "Y" + "#" '构造发送命令字符串
    DevWriteStr(strSend) '发送命令
    sendnum=sendnum+1   '记录已发送命令次数
    '!SetSingleChannelValueByNum() 这部分是示例注释，根据实际情况设置通道值
END IF
```

### 注意事项

- 在实际应用中，需根据具体的通讯协议来定制`strSend`中的内容。
- `DevWriteStr()`函数用于发送串口数据，而接收数据处理则需配置相应的事件或定时器触发的脚本以完成数据的读取与解析。
- CRC校验是确保数据完整性的关键环节，具体实现方式应符合你的通讯协议要求。
- 脚本中的变量定义和逻辑控制语句（如IF条件、循环）应当按照实际的数据交互逻辑进行调整。

## 结论

掌握MCGS的串口驱动脚本编程能力，能极大提升设备控制的灵活性和效率。上述示例仅为入门级操作，针对复杂应用场景，还需要深入了解MCGS软件的高级功能以及深入学习通讯协议的知识。希望此文档能为你在MCGS串口通讯方面的开发工作提供帮助。

## 下载链接

[MCGS串口驱动说明文档](https://pan.quark.cn/s/15117bf2eba2)