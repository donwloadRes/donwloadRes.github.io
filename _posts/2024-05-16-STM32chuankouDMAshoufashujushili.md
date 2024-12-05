---
layout: post
title: "STM32串口DMA收发数据示例"
date:   2021-10-21
tags: [DMA,USART,InitStruct,串口,收发]
comments: true
author: admin
---
# STM32串口DMA收发数据示例

## 项目描述

本项目提供了一个基于STM32的串口DMA收发数据示例，适用于STM32F103系列微控制器。该示例经过稳定测试，初始化后可直接使用，帮助开发者快速理解和实现串口DMA数据收发功能。

## 功能特点

- **DMA收发**：通过DMA（直接内存访问）实现串口数据的收发，减少CPU的负担，提高数据传输效率。
- **稳定可靠**：经过严格测试，确保代码的稳定性和可靠性。
- **易于集成**：代码结构清晰，易于集成到其他STM32项目中。

## 使用说明

1. **硬件准备**：
   - 使用STM32F103系列微控制器。
   - 连接串口设备（如PC或其他微控制器）。

2. **软件准备**：
   - 使用STM32CubeMX生成初始化代码。
   - 将本项目中的代码集成到生成的工程中。

3. **配置串口和DMA**：
   - 根据实际需求配置串口参数（波特率、数据位、停止位等）。
   - 配置DMA通道，确保DMA能够正确处理串口数据的收发。

4. **编译和下载**：
   - 编译工程并下载到STM32微控制器中。
   - 启动程序，观察串口数据收发情况。

## 示例代码

```c
// 示例代码片段
void USART1_DMA_Init(void)
{
    // 配置串口
    USART_InitTypeDef USART_InitStruct = {0};
    USART_InitStruct.USART_BaudRate = 9600;
    USART_InitStruct.USART_WordLength = USART_WordLength_8b;
    USART_InitStruct.USART_StopBits = USART_StopBits_1;
    USART_InitStruct.USART_Parity = USART_Parity_No;
    USART_InitStruct.USART_Mode = USART_Mode_Rx | USART_Mode_Tx;
    USART_InitStruct.USART_HardwareFlowControl = USART_HardwareFlowControl_None;
    USART_Init(USART1, &USART_InitStruct);

    // 配置DMA
    DMA_InitTypeDef DMA_InitStruct = {0};
    DMA_InitStruct.DMA_PeripheralBaseAddr = (uint32_t)&USART1->DR;
    DMA_InitStruct.DMA_MemoryBaseAddr = (uint32_t)TxBuffer;
    DMA_InitStruct.DMA_DIR = DMA_DIR_PeripheralDST;
    DMA_InitStruct.DMA_BufferSize = sizeof(TxBuffer);
    DMA_InitStruct.DMA_PeripheralInc = DMA_PeripheralInc_Disable;
    DMA_InitStruct.DMA_MemoryInc = DMA_MemoryInc_Enable;
    DMA_InitStruct.DMA_PeripheralDataSize = DMA_PeripheralDataSize_Byte;
    DMA_InitStruct.DMA_MemoryDataSize = DMA_MemoryDataSize_Byte;
    DMA_InitStruct.DMA_Mode = DMA_Mode_Normal;
    DMA_InitStruct.DMA_Priority = DMA_Priority_High;
    DMA_InitStruct.DMA_M2M = DMA_M2M_Disable;
    DMA_Init(DMA1_Channel4, &DMA_InitStruct);

    // 启动DMA和串口
    DMA_Cmd(DMA1_Channel4, ENABLE);
    USART_DMACmd(USART1, USART_DMAReq_Tx, ENABLE);
    USART_Cmd(USART1, ENABLE);
}
```

## 贡献

欢迎开发者提交问题、建议或改进代码。请通过GitHub的Issue或Pull Request功能进行贡献。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 联系我们

如有任何问题或建议，请联系项目维护者：[你的邮箱地址]。

## 下载链接

[STM32串口DMA收发数据示例](https://pan.quark.cn/s/e9fa90d1bb34)