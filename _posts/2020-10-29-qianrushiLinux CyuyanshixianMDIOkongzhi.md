---
layout: post
title: "嵌入式Linux C语言实现MDIO控制"
date:   2022-03-30
tags: [MDIO,mdio,PHY,gcc,arm]
comments: true
author: admin
---
# 嵌入式Linux C语言实现MDIO控制

## 项目描述

本项目提供了一个嵌入式Linux环境下使用C语言实现MDIO（Management Data Input/Output）控制的资源文件。通过修改交叉编译配置，实现了MDIO指令的自定义功能。MDIO是一种用于管理以太网PHY（物理层）设备的接口协议，通过该接口可以读取和写入PHY的寄存器，从而实现对PHY设备的配置和监控。

## 功能说明

- **MDIO读取操作**：通过`mdio read 0 1`指令，可以读取PHY的广播地址为0，PHY地址为1的寄存器值。
- **MDIO写入操作**：通过`mdio eth0 write 0 0 0x12`指令，可以向PHY地址为0的寄存器写入值`0x12`。
- **交叉编译配置**：项目中使用了Linaro交叉编译工具链，具体路径为`/home/fmsh/work/FMQL-Linux-SDK/gcc-linaro-7.3.1-2018.05-x86_64_arm-linux-gnueabihf/bin/arm-linux-gnueabihf-gcc`。

## 使用方法

1. **编译**：
   使用以下命令进行编译：
   ```bash
   make
   ```
   编译成功后会生成可执行文件`mdio`。

2. **运行**：
   将生成的可执行文件`mdio`拷贝到目标嵌入式设备上，并根据需要执行MDIO读写操作。

3. **清理**：
   使用以下命令清理编译生成的文件：
   ```bash
   make clean
   ```

## Makefile说明

```makefile
arm_cross_gcc = /home/fmsh/work/FMQL-Linux-SDK/gcc-linaro-7.3.1-2018.05-x86_64_arm-linux-gnueabihf/bin/arm-linux-gnueabihf-gcc
objects = mdio.o

mdio: $(objects)
	$(arm_cross_gcc) -o mdio $(objects)

%.o : %.c
	$(arm_cross_gcc) -c $<

.PHONY: clean
clean:
	rm mdio $(objects)
	@echo clean finish
```

## 注意事项

- 在执行MDIO操作时，PHY地址需要从设备树中获取。
- 确保交叉编译工具链路径正确，否则编译会失败。

## 贡献

欢迎提交Issue和Pull Request，共同完善该项目。

## 下载链接

[嵌入式LinuxC语言实现MDIO控制](https://pan.quark.cn/s/1b3850676607)