---
layout: post
title: "Python查找在圆周率100万个数字中是否有你的生日"
date:   2023-02-04
tags: [圆周率,生日,100,str,查找]
comments: true
author: admin
---
# Python查找在圆周率100万个数字中是否有你的生日

本仓库提供了一个Python脚本，用于查找你的生日是否存在于圆周率的前100万个数字中。通过这个脚本，你可以验证你的生日是否在圆周率的数字序列中出现。

## 使用方法

1. **下载资源文件**：
   - 下载本仓库中的资源文件，该文件包含了圆周率的前100万个数字。

2. **运行Python脚本**：
   - 使用Python运行提供的脚本，输入你的生日（格式如：19980101）。
   - 脚本将自动在圆周率的数字序列中查找你的生日，并返回查找结果。

## 示例

```python
# 示例代码
with open('pai.txt', 'r', encoding="UTF-8") as f:
    str = f.readlines()
    pi_str = ''
    for line in str:
        pi_str += line.rstrip()

while True:
    day = input('请输入你的生日(如：19980101)\n')
    if day:
        have = pi_str.find(day)
        if have == -1:
            print('在前100万个圆周率数字里面没有发现和你生日相同的，换另一个吧。')
        else:
            print('你的生日在圆周率pi的第', have, '个')
            print('         ' + '\033[36m' + pi_str[int(have): int(have) + len(day)] + '\033[0m' + pi_str[int(have) + len(day): (int(have) + len(day) + 6)] + '         ')
    else:
        print('查找不到或者重新输入')
```

## 注意事项

- 确保你已经安装了Python环境。
- 资源文件路径需要根据实际情况进行调整。
- 脚本仅适用于查找圆周率前100万个数字中的生日，不支持更大范围的查找。

通过这个脚本，你可以轻松验证你的生日是否在圆周率的前100万个数字中出现。

## 下载链接

[Python查找在圆周率100万个数字中是否有你的生日](https://pan.quark.cn/s/c9118f3b77dd)