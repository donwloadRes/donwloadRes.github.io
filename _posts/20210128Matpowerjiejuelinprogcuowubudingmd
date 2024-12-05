---
layout: post
title: "Matpower解决linprog错误补丁"
date:   2021-03-03
tags: [补丁,Matpower,test,Error,qps]
comments: true
author: admin
---
# Matpower解决linprog错误补丁

## 描述

本资源文件提供了一个针对Matpower版本7.1和8.0的错误补丁，适用于MATLAB R2023a。当您在运行`test_matpower`或`test_most`时遇到以下错误时，可以使用此补丁：

```
Error using linprog
LINPROG(fAbAeqbeqLBUBX0OPTIONS) does not accept X0. Use LINPROG(fAbAeqbeqLBUBOPTIONS) instead.
Error in qps_ot (line 268)
linprog(c Ai bi Ae be xmin xmax x0 ot_opt);
Error in qps_master (line 266)
qps_ot(H c A l u xmin xmax x0 opt);
Error in t_qps_master (line 107)
[x f s out lam] = qps_master([] c A l u xmin [] [] opt);
Error in t_run_test
```

此补丁已经过亲测，可以有效解决上述问题。

## 使用方法

1. 下载本资源文件。
2. 将补丁文件替换或合并到您的Matpower安装目录中。
3. 重新运行`test_matpower`或`test_most`，确认错误已解决。

## 注意事项

- 请确保您的Matpower版本为7.1或8.0。
- 本补丁仅适用于MATLAB R2023a。

希望本补丁能帮助您顺利解决Matpower运行中的问题。如有任何疑问或建议，请随时联系我们。

## 下载链接

[Matpower解决linprog错误补丁](https://pan.quark.cn/s/4042b409d469)