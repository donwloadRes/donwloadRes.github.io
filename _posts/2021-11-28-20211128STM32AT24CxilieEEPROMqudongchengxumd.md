---
layout: post
title: "STM32 AT24C系列EEPROM驱动程序"
date:   2022-11-03
tags: [AT24C,驱动程序,STM32,EEPROM,I2C]
comments: true
author: admin
---
# STM32 AT24C系列EEPROM驱动程序

## 简介
本仓库提供了一套基于STM32的AT24C系列EEPROM驱动程序，包括AT24C32、AT24C64和AT24C128的驱动。该驱动程序采用模拟I2C通信方式，具有良好的移植性和易用性，用户只需修改两个IO口即可轻松适配不同的硬件平台。

## 功能特点
- **模拟I2C驱动**：采用软件模拟I2C通信，无需硬件I2C外设，适用于所有STM32系列芯片。
- **易于移植**：驱动代码结构清晰，用户只需修改两个IO口的配置即可在不同硬件平台上使用。
- **支持多种容量**：支持AT24C32、AT24C64和AT24C128三种不同容量的EEPROM芯片。
- **高效可靠**：经过测试验证，驱动程序稳定可靠，适用于各种嵌入式应用场景。

## 使用方法
1. **克隆仓库**：
   ```bash
   git clone https://github.com/yourusername/STM32_AT24C_Driver.git
   ```

2. **配置IO口**：
   打开`at24c_driver.h`文件，根据实际硬件连接修改以下两个宏定义：
   ```c
   #define AT24C_SCL_PIN  GPIO_PIN_6
   #define AT24C_SDA_PIN  GPIO_PIN_7
   ```

3. **集成到项目**：
   将驱动文件`at24c_driver.c`和`at24c_driver.h`添加到你的STM32项目中，并在主程序中调用相关API进行读写操作。

4. **编译运行**：
   编译并下载程序到STM32开发板，验证驱动程序的功能。

## API说明
- **初始化函数**：
  ```c
  void AT24C_Init(void);
  ```
  初始化AT24C系列EEPROM的I2C通信。

- **写入数据函数**：
  ```c
  uint8_t AT24C_WriteByte(uint16_t addr, uint8_t data);
  ```
  向指定地址写入一个字节的数据。

- **读取数据函数**：
  ```c
  uint8_t AT24C_ReadByte(uint16_t addr);
  ```
  从指定地址读取一个字节的数据。

## 示例代码
以下是一个简单的示例代码，演示如何使用该驱动程序进行数据读写：
```c
#include "at24c_driver.h"

int main(void) {
    // 初始化AT24C驱动
    AT24C_Init();

    // 向地址0x00写入数据0xAA
    AT24C_WriteByte(0x00, 0xAA);

    // 从地址0x00读取数据
    uint8_t data = AT24C_ReadByte(0x00);

    // 验证读取的数据
    if (data == 0xAA) {
        // 读取成功
    } else {
        // 读取失败
    }

    while (1) {
        // 主循环
    }
}
```

## 贡献
欢迎大家提交Issue和Pull Request，共同完善本驱动程序。

## 许可证
本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 联系我们
如有任何问题或建议，请联系：[your.email@example.com](mailto:your.email@example.com)

## 下载链接

[STM32AT24C系列EEPROM驱动程序](https://pan.quark.cn/s/1d24b84b7270)