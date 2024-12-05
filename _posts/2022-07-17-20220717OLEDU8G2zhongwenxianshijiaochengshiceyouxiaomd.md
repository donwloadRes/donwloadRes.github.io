---
layout: post
title: "OLED U8G2 中文显示教程实测有效"
date:   2020-12-30
tags: [u8g2,文件,中文,OLED,font]
comments: true
author: admin
---
# OLED U8G2 中文显示教程（实测有效）

## 简介
本资源文件详细介绍了如何在OLED显示屏上使用U8G2库显示中文。通过本教程，您可以轻松地在OLED屏幕上显示自定义的中文字符，解决中文显示不全或无法显示的问题。

## 环境准备
- 操作系统：Windows 10
- IDE：Arduino
- 开发板：ESP8266
- 显示器：0.96寸OLED液晶屏
- 引脚连接：D1–SOA, D2–SCL, 3V3–VCC, G–GND
- 库包：U8G2

## 操作步骤

### 第一步：Unicode编码转换
1. 打开一个Unicode编码转换网站，将需要显示的中文字符转换为Unicode编码。
2. 例如，将“想输的字”转换为Unicode编码：\u60f3\u8f93\u7684\u5b57。

### 第二步：修改Unicode编码
1. 将获取到的Unicode编码字符串中的`\u`替换为`$`。
2. 将字符串中的英文部分转换为大写，例如：$60F3 $8F93 $7684 $5B57。

### 第三步：生成字库文件
1. 找到Windows系统字体文件，将其放在新建的文件夹中。
2. 使用GuiTool工具生成字库文件，生成simsun_U16.bdf和simsun_U16.bin两个文件。

### 第四步：配置统一码map文件
1. 将统一码map文件夹中的chinese.map文件用编辑器打开。
2. 将第二步中获取到的字符串添加到chinese.map文件的最前面，并保存。
3. 将chinese.map文件放到生成的字库文件目录下。

### 第五步：生成u8g2_font_unifont_zgzt.c文件
1. 将bdfconv文件夹中的bdfconv.exe和转换.bat文件放在字库文件目录下。
2. 右击转换.bat文件选择编辑，确保文件名与生成的字库文件一致。
3. 双击转换.bat文件，生成u8g2_font_unifont_zgzt.c文件。

### 第六步：替换字体内容
1. 打开u8g2_font_unifont_zgzt.c文件，复制等号后面的所有内容。
2. 找到Arduino库文件夹中的u8g2库，打开u8g2_fonts.c文件。
3. 搜索u8g2_font_unifont_t_chinese1，用新生成的内容替换原有内容并保存。

### 第七步：编写Arduino代码
1. 打开Arduino IDE，编写代码以使用U8G2库显示中文。
2. 确保使用替换后的u8g2_font_unifont_t_chinese1字体。

## 注意事项
- 确保u8g2_SetFont()函数使用的是替换后的u8g2_font_unifont_t_chinese1字体。
- 编译并上传代码后，中文即可成功显示在OLED屏幕上。

通过以上步骤，您可以成功在OLED屏幕上显示自定义的中文字符。希望本教程对您有所帮助！

## 下载链接

[OLEDU8G2中文显示教程实测有效分享](https://pan.quark.cn/s/72df9136cec8)