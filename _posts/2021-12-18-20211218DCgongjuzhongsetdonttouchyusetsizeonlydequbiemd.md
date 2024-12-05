---
layout: post
title: "DC工具中setdonttouch与setsizeonly的区别"
date:   2023-09-17
tags: [set,DC,dont,touch,size]
comments: true
author: admin
---
# DC工具中set_dont_touch与set_size_only的区别

在数字电路设计流程中，综合（Synthesis）是一个关键步骤，它将高级语言描述（如Verilog）转换成门级网表。Design Compiler (DC) 是业界广泛使用的综合工具之一。在进行综合时，设计者经常需要控制某些模块或对象不被修改或仅考虑其大小，这时就涉及到了`set_dont_touch`和`set_size_only`两个重要命令。本文档旨在详细解释这两个命令在DC中的具体用途及它们之间的区别。

## set_dont_touch

### 定义：
`set_dont_touch`命令用于指定某个设计单元不应被DC优化、移动或者删除。这个设置适用于那些需要维持原样的IP核、时钟结构或是其他对性能至关重要的硬宏模块。一旦应用了此指令，DC会完全避开这些区域，确保它们保持设计者的原始定义。

### 应用场景：
- 保护已知最佳实现的模块。
- 确保知识产权(IP)核心不变。
- 维持特定逻辑的精确延时特性。

## set_size_only

### 定义：
与`set_dont_touch`不同，`set_size_only`命令指示DC可以调整指定设计单元的内部逻辑以满足面积约束，但其I/O端口和总体大小应保持不变。这意味着DC可以改变模块的内部实现来优化资源使用，同时保持外部接口不变和逻辑功能的完整。

### 应用场景：
- 当需要固定模块接口且希望内部尽可能优化时使用。
- 在面积敏感而功能无需更改的应用中特别有用。

## 主要区别

1. **交互性**：`set_dont_touch`保护模块的完整性，不允许任何改动；而`set_size_only`允许内部改动，只要不影响外接界面和整体尺寸。
2. **优化范围**：前者完全排除优化，后者只限制在保留外部接口和尺寸条件下进行优化。
3. **适用对象**：通常，对于外部供应商提供的IP或者经过严格验证的核心逻辑，选择`set_dont_touch`更为合适；而对于需要保持尺寸稳定但内部可以适度优化的模块，则采用`set_size_only`。

总之，在Design Compiler的综合过程中，根据设计需求明智地选择和应用`set_dont_touch`和`set_size_only`，可以有效地平衡设计的性能、面积和重用性，确保设计质量的同时满足项目目标。

## 下载链接

[DC工具中set_dont_touch与set_size_only的区别](https://pan.quark.cn/s/e025666f782f)