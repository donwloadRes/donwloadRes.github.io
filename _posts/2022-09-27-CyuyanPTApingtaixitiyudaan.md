---
layout: post
title: "C语言PTA平台习题与答案"
date:   2023-10-21
tags: [C语言,int,答案,习题,题目]
comments: true
author: admin
---
# C语言PTA平台习题与答案

## 资源描述

本资源文件包含了C语言PTA平台上的部分习题答案，涵盖了基础的C语言编程题目。以下是部分题目的答案示例：

### 题目1：输出短句

**题目要求**：编写程序，输出一个短句“Welcome to You!”

**答案代码**：
```c
#include<stdio.h>
int main(){
    printf("Welcome to You!\n");
    return 0;
}
```

### 题目2：华氏温度转换为摄氏温度

**题目要求**：编写程序，计算华氏温度100°F对应的摄氏温度。计算公式：C = 5 × (F − 32) / 9，式中：C表示摄氏温度，F表示华氏温度，输出数据要求为整型。

**答案代码**：
```c
#include<stdio.h>
int main(){
    int fahr = 100;
    int celsius = 5 * (fahr - 32) / 9;
    printf("fahr = 100; celsius = %d\n", celsius);
    return 0;
}
```

### 题目3：求整数均值

**题目要求**：编写程序，计算4个整数的和与平均值。题目保证输入与输出均在整型范围内。在一行中按照格式“Sum = 和; Average = 平均值”顺序输出和与平均值，其中平均值精确到小数点后一位。

**答案代码**：
```c
#include<stdio.h>
int main(){
    int a, b, c, d;
    scanf("%d %d %d %d", &a, &b, &c, &d);
    int sum = a + b + c + d;
    double average = sum / 4.0;
    printf("Sum = %d; Average = %.1f\n", sum, average);
    return 0;
}
```

## 使用说明

1. **下载资源**：您可以直接下载本仓库中的资源文件，获取C语言PTA平台上的习题答案。
2. **参考学习**：建议您在参考答案的基础上，尝试自己编写代码，理解每一步的逻辑和实现方式。
3. **自主练习**：通过这些习题的练习，您可以更好地掌握C语言的基础编程知识，提升编程能力。

## 注意事项

- 请勿直接抄袭答案，理解代码的实现原理才是学习的关键。
- 如果在使用过程中遇到问题，欢迎提出Issue，我们会尽快回复并提供帮助。

希望本资源能够帮助您更好地学习和掌握C语言编程！

## 下载链接

[C语言PTA平台习题与答案](https://pan.quark.cn/s/affb3c32e3f5)