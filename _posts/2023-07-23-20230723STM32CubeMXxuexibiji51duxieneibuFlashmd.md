---
layout: post
title: "STM32CubeMX学习笔记（51）——读写内部Flash"
date:   2024-11-23
tags: [Flash,STM32,内部,写入,STM32CubeMX]
comments: true
author: admin
---
# STM32CubeMX学习笔记（51）——读写内部Flash

本资源文件详细介绍了如何使用STM32CubeMX工具进行STM32芯片内部Flash的读写操作。通过本教程，您将学习到如何在STM32芯片上配置和操作内部Flash存储器，包括如何解锁、擦除、写入和读取数据。

## 内容概述

1. **简介**  
   介绍了STM32芯片内部Flash的基本概念和用途，包括主存储器、系统存储器和选项字节的地址分布及大小。

2. **新建工程**  
   详细说明了如何使用STM32CubeMX工具创建一个新的工程，并配置时钟和调试模式。

3. **添加串口打印**  
   介绍了如何在工程中添加串口打印功能，以便查看调试信息。

4. **生成代码**  
   说明了如何生成代码并配置开发环境，以便进行后续的开发工作。

5. **查看工程的空间分布**  
   介绍了如何查看工程在内部Flash中的存储分布，以确保不会误操作覆盖程序代码。

6. **官方HAL库Flash操作常见函数**  
   列出了STM32官方HAL库中常用的Flash操作函数，包括解锁、锁定、写入、擦除和等待操作完成等。

7. **读取Flash**  
   详细说明了如何读取内部Flash中的数据，并提供了相应的代码示例。

8. **写入Flash**  
   详细说明了如何向内部Flash写入数据，包括解锁、擦除页和写入数据的具体步骤。

9. **举例**  
   提供了一个完整的示例代码，展示了如何在STM32芯片上进行Flash的读写操作。

## 注意事项

- 在进行Flash操作时，务必确保不会误操作覆盖程序代码。
- 用户代码应放置在`USER CODE BEGIN N`和`USER CODE END N`之间，以避免在重新生成代码时被删除。

通过本教程，您将能够熟练掌握STM32芯片内部Flash的读写操作，为后续的嵌入式开发工作打下坚实的基础。

## 下载链接

[STM32CubeMX学习笔记51读写内部Flash](https://pan.quark.cn/s/a8f3848092e8)