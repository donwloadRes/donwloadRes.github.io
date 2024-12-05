---
layout: post
title: "jieba分词与停用词处理工具
date   20210120
tags jieba用词txt分词stopwords
comments true
author admin

 jieba分词与停用词处理工具

 简介

本资源文件提供了一个使用Python和jieba库进行中文文本分词并去除停用词的工具该工具可以将处理后的文本保存到新的txt文件中方便后续的自然语言处理任务

 功能特点

 jieba分词使用jieba库对中文文本进行分词支持精确模式和全模式
 去除停用词加载自定义的停用词列表去除文本中的无意义词汇
 保存结果将处理后的文本保存到新的txt文件中便于后续分析和使用

 使用方法

1 安装依赖
   bash
   pip install jieba
   

2 配置停用词列表
   将停用词列表保存为stopwordstxt文件每行一个停用词

3 运行脚本
   将待处理的文本文件保存为origindatayutxt运行脚本后处理结果将保存为yuliao3txt

 代码示例

python
import jieba

 创建停用词list
def stopwordslistfilepath
    stopwords  linestrip for line in openfilepath r encodingutf8readlines
    return stopwords

 对句子进行分词
def segsentencesentence
    sentenceseged  jiebacutsentencestrip
    stopwords  stopwordsliststopwordstxt   这里加载停用词的路径
    outstr  
    for word in sentenceseged
        if word not in stopwords
            if word  t
                outstr  word
                outstr   "
date:   2021-01-20
tags: [jieba,用词,txt,分词,stopwords]
comments: true
author: admin
---
# jieba分词与停用词处理工具

## 简介

本资源文件提供了一个使用Python和jieba库进行中文文本分词，并去除停用词的工具。该工具可以将处理后的文本保存到新的txt文件中，方便后续的自然语言处理任务。

## 功能特点

- **jieba分词**：使用jieba库对中文文本进行分词，支持精确模式和全模式。
- **去除停用词**：加载自定义的停用词列表，去除文本中的无意义词汇。
- **保存结果**：将处理后的文本保存到新的txt文件中，便于后续分析和使用。

## 使用方法

1. **安装依赖**：
   ```bash
   pip install jieba
   ```

2. **配置停用词列表**：
   将停用词列表保存为`stopwords.txt`文件，每行一个停用词。

3. **运行脚本**：
   将待处理的文本文件保存为`origin_data/yu.txt`，运行脚本后，处理结果将保存为`yuliao3.txt`。

## 代码示例

```python
import jieba

# 创建停用词list
def stopwordslist(filepath):
    stopwords = [line.strip() for line in open(filepath, 'r', encoding='utf-8').readlines()]
    return stopwords

# 对句子进行分词
def seg_sentence(sentence):
    sentence_seged = jieba.cut(sentence.strip())
    stopwords = stopwordslist('stopwords.txt')  # 这里加载停用词的路径
    outstr = ''
    for word in sentence_seged:
        if word not in stopwords:
            if word != '\t':
                outstr += word
                outstr += " "
    return outstr

inputs = open('origin_data/yu.txt', 'r', encoding='utf-8')
outputs = open('yuliao3.txt', 'w', encoding='utf-8')

for line in inputs:
    line_seg = seg_sentence(line)  # 这里的返回值是字符串
    outputs.write(line_seg + '\n')

outputs.close()
inputs.close()
```

## 注意事项

- 确保停用词列表文件路径正确。
- 处理后的文本文件路径可以根据需要进行调整。

## 参考资料

- [jieba分词库官方文档](https://github.com/fxsjy/jieba)
- [Python中文分词工具之jieba](https://blog.csdn.net/qq_27492735/article/details/82082233)

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个工具。

## 下载链接

[jieba分词与停用词处理工具分享](https://pan.quark.cn/s/870beb60459a)