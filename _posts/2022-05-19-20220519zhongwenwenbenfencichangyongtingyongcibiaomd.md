---
layout: post
title: "中文文本分词常用停用词表
date   20230907
tags 词表停用stopwordstxt分词
comments true
author admin

 中文文本分词常用停用词表

本仓库提供了一系列常用的中文停用词表这些停用词表在处理中文文本分词时非常有用特别是在使用jieba分词工具时以下是本仓库提供的停用词表及其对应的文件名

 中文停用词表 cnstopwordstxt
 哈工大停用词表 hitstopwordstxt
 百度停用词表 baidustopwordstxt
 四川大学机器智能实验室停用词库 scustopwordstxt

 使用方法

在使用jieba分词工具时可以通过以下方式载入停用词表

python
import jieba

 读取停用词表
stopwords  set
with openpathtostopwordsfiletxt r encodingutf8 as f
    for line in f
        stopwordsaddlinestrip

 分词并过滤停用词
text  这是一个需要分词的文本"
date:   2023-09-07
tags: [词表,停用,stopwords,txt,分词]
comments: true
author: admin
---
# 中文文本分词常用停用词表

本仓库提供了一系列常用的中文停用词表，这些停用词表在处理中文文本分词时非常有用，特别是在使用jieba分词工具时。以下是本仓库提供的停用词表及其对应的文件名：

- **中文停用词表**: `cn_stopwords.txt`
- **哈工大停用词表**: `hit_stopwords.txt`
- **百度停用词表**: `baidu_stopwords.txt`
- **四川大学机器智能实验室停用词库**: `scu_stopwords.txt`

## 使用方法

在使用jieba分词工具时，可以通过以下方式载入停用词表：

```python
import jieba

# 读取停用词表
stopwords = set()
with open('path_to_stopwords_file.txt', 'r', encoding='utf-8') as f:
    for line in f:
        stopwords.add(line.strip())

# 分词并过滤停用词
text = "这是一个需要分词的文本"
words = jieba.lcut(text)
filtered_words = [word for word in words if word not in stopwords]

print(filtered_words)
```

请将`path_to_stopwords_file.txt`替换为实际的停用词表文件路径。

## 文件说明

- `cn_stopwords.txt`: 中文停用词表
- `hit_stopwords.txt`: 哈工大停用词表
- `baidu_stopwords.txt`: 百度停用词表
- `scu_stopwords.txt`: 四川大学机器智能实验室停用词库

## 贡献

欢迎贡献更多的停用词表或改进现有的停用词表。请提交Pull Request或Issue。

## 许可证

本仓库的内容遵循MIT许可证。详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[中文文本分词常用停用词表](https://pan.quark.cn/s/484644761134)

## 下载链接

[中文文本分词常用停用词表](https://pan.quark.cn/s/96b3bbeac6b4)