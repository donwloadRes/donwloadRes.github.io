---
layout: post
title: "京东自动抢购脚本抢购茅台"
date:   2023-03-16
tags: [抢购,京东,登录,自动,requirements]
comments: true
author: admin
---
# 京东自动抢购脚本-抢购茅台

## 项目描述
本项目提供一个自动化脚本，用于在京东商城（www.jd.com）上自动预约和抢购茅台酒。用户可以通过京东APP扫码登录或使用账号密码登录，并设置定时任务来自动执行预约和抢购操作。

## 主要功能
- 登录京东商城
- 自动预约茅台酒
- 定时自动预约和抢购

## 运行环境
- Python 3.8

## 第三方库
项目所需的第三方库已列在`requirements.txt`文件中。可以使用以下指令进行安装：
```bash
pip install -r requirements.txt
```
如果国内安装第三方库较慢，可以使用清华源加速：
```bash
pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple/
```

## 使用教程
1. **推荐使用Chrome浏览器**
2. **登录方式**
   - 网页扫码登录
   - 账号密码登录
3. **配置信息**
   - 填写`config.ini`文件中的配置信息
   - `eid`和`fp`的获取方法：
     - 找一个普通商品随便下单，然后进入结算页面
     - 打开浏览器的调试窗口，切换到控制台Tab页
     - 在控制台中输入变量`_JdTdudfp`，即可从输出的Json中获取`eid`和`fp`
     - 如果不清楚如何操作，可以参考原作者的issue：[链接](https://g)

## 注意事项
- 请确保Python环境已正确安装
- 配置文件中的信息需根据实际情况填写
- 请遵守京东商城的相关规定，合理使用自动化脚本

## 贡献
欢迎大家贡献代码，提出问题和建议。请通过GitHub的issue系统进行反馈。

## 许可证
本项目采用MIT许可证，详情请参阅`LICENSE`文件。

## 下载链接

[京东自动抢购脚本-抢购茅台](https://pan.quark.cn/s/b50de23fc7bc)