---
layout: post
title: "STM32F103 HAL库驱动0.96寸OLED显示屏"
date:   2023-04-08
tags: [OLED,HAL,代码,IIC,STM32CubeMX]
comments: true
author: admin
---
# STM32F103 HAL库驱动0.96寸OLED显示屏

## 简介
本仓库提供了一个基于STM32F103微控制器的0.96寸OLED显示屏驱动程序，该程序已从标准库移植至HAL库。使用模拟IIC接口，引脚配置灵活可调，方便用户根据实际需求进行二次开发。驱动程序通过STM32CubeMX进行配置，简化了开发流程。

## 功能特点
- **HAL库移植**：将原本基于标准库的OLED驱动代码移植到HAL库，提高了代码的可读性和可维护性。
- **模拟IIC接口**：采用模拟IIC通信方式，用户可以根据需要灵活配置IIC引脚。
- **STM32CubeMX配置**：使用STM32CubeMX进行硬件配置，简化了初始化过程，便于快速上手。
- **易于二次开发**：代码结构清晰，注释详细，方便用户进行功能扩展和定制。

## 使用说明
1. **硬件准备**：
   - STM32F103开发板
   - 0.96寸OLED显示屏
   - 连接线若干

2. **软件准备**：
   - STM32CubeMX
   - Keil uVision或其他STM32开发环境

3. **配置步骤**：
   - 使用STM32CubeMX生成基础的HAL库工程。
   - 将本仓库提供的驱动代码文件添加到工程中。
   - 根据实际硬件连接情况，配置IIC引脚。
   - 编译并下载程序到STM32F103开发板。

4. **代码结构**：
   - `oled.c` 和 `oled.h`：OLED显示屏驱动核心代码。
   - `main.c`：主程序文件，包含初始化和示例显示代码。

## 示例代码
以下是一个简单的示例代码，展示如何在OLED显示屏上显示文本：

```c
#include "main.h"
#include "oled.h"

int main(void)
{
    HAL_Init();
    SystemClock_Config();
    OLED_Init();

    OLED_Clear();
    OLED_ShowString(0, 0, "Hello, World!", 16);

    while (1)
    {
        // 主循环
    }
}
```

## 贡献
欢迎各位开发者贡献代码，提出问题和建议。请通过GitHub的Issue和Pull Request功能进行交流。

## 许可证
本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 联系我们
如有任何问题或建议，请联系项目维护者：
- 邮箱：[your-email@example.com]
- GitHub：[your-github-username]

感谢您的关注和支持！

## 下载链接

[STM32F103HAL库驱动0.96寸OLED显示屏](https://pan.quark.cn/s/22dcace0fcca)