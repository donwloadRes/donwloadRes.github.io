---
layout: post
title: "M3u8文件合并为Mp4工具"
date:   2020-06-16
tags: [文件,文件夹,m3u8,key,工具]
comments: true
author: admin
---
# M3u8文件合并为Mp4工具

## 简介
本工具旨在帮助用户将通过UC浏览器下载的m3u8文件（包含一个m3u8文件和一个对应的文件夹）转换为mp4格式。即使m3u8文件带有密钥（key），本工具也能正常处理。

## 环境要求
- 需要配置有jre1.8。如果尚未安装，请在网上搜索如何安装，并确保安装后配置好环境变量。

## 适用文件
- m3u8对应的文件夹里，文件命名应为0，1，2，3……等数字，且没有后缀名。
- 可能会有0.key之类的文件（也可能没有），该文件是密钥文件，是有用的。
- 如果有不是0，1，2，3……来命名，且不是.key的文件，这些文件将不会被使用（正常情况下，这些文件也是没有用的）。

## 使用方式
1. 尽可能保证input文件夹和out文件夹是空的。
2. 将下载的m3u8文件和对应的文件夹，都放在input文件夹中。
3. 双击M3u8ToMp4.exe执行。
4. 执行完成后，output文件夹中会生成对应的mp4文件。

## 注意事项
- exe所在的路径尽量不要有中文，以避免可能的兼容性问题。

## 贡献
欢迎大家贡献代码，提出问题或建议，共同完善本工具。

## 许可证
本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[M3u8文件合并为Mp4工具](https://pan.quark.cn/s/2d77e8cccc99)