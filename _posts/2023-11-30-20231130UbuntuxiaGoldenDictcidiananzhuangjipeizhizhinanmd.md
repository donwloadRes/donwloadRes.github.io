---
layout: post
title: "Ubuntu下GoldenDict词典安装及配置指南"
date:   2021-07-22
tags: [词典,En,GoldenDict,Ubuntu,sudo]
comments: true
author: admin
---
# Ubuntu下GoldenDict词典安装及配置指南

## 简介
本资源文件提供了在Ubuntu系统下安装和配置GoldenDict词典的详细步骤。GoldenDict是一款功能强大的跨平台词典软件，支持多种词典格式，并且可以集成在线翻译服务。

## 安装步骤

### 1. 安装GoldenDict和WordNet
首先，使用以下命令安装GoldenDict和WordNet：
```bash
sudo apt-get install goldendict goldendict-wordnet
```
安装完成后，您可以使用GoldenDict来查询单词，默认会显示WordNet词库中的词条。

### 2. 下载并配置词典
为了获得更丰富的词典资源，您需要下载一些离线词典文件。以下是一些推荐的词典：
- **Oxford Advanced Learner’s Dictionary 8th edition (En-En)** - 牛津高阶词典（英英）第8版，含图片及英式发音和美式发音。
- **Merriam-Webster’s Collegiate 11th edition (En-En)** - 韦氏大学词典（英英）第11版，含图片及发音。
- **Longman DOCE5 (En-En)** - 朗文当代第五版英英词典，含发音和图片，大部分例句也带有朗读。
- **Longman Pronunciation Dictionary 3rd edition (En-En)** - 朗文发声辞典第三版，词典中有英音、美音，并对于“多音”的词，配有preference poll图表。
- **Longman DOCE5 Extras (En-En)** - 不包含单词发音和图片，但是包含了该词汇的各种搭配。
- **Oxford Advanced Learner’s Dictionary 4th edition (En-zh_CN)** - 牛津高阶英汉双解第四版，英汉双解，对于国人来说是必不可少的。

将下载的词典文件解压到您选择的目录中，然后在GoldenDict中设置词典目录并加载。

### 3. 配置词形匹配
为了解决Goldendict在查询复数形式（如“books”）时无法自动转换为单数形式（如“book”）的问题，您需要配置词形匹配规则。下载并解压英文构词法规则库文件，然后在GoldenDict中设置其路径。

## 其他配置

### 播放离线词库中的语音
如果需要播放离线词库中的语音，您还需要安装mplayer及其解码器：
```bash
sudo apt-get install mplayer
sudo apt-get install ubuntu-restricted-addons
sudo apt-get install ubuntu-restricted-extras
```

## 结语
通过以上步骤，您可以在Ubuntu系统上成功安装并配置GoldenDict词典，享受丰富的词典资源和便捷的查询体验。

## 下载链接

[Ubuntu下GoldenDict词典安装及配置指南分享](https://pan.quark.cn/s/f9117a58d528)