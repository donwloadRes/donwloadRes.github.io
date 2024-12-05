---
layout: post
title: "Python之红楼梦词频统计并生成图云"
date:   2021-04-26
tags: [词云,txt,词频,红楼梦,Python]
comments: true
author: admin
---
# Python之红楼梦词频统计并生成图云

本仓库提供了完整的Python脚本和指南，帮助您分析古典名著《红楼梦》中的词频，并自动生成美观的词云图像。这份资源非常适合学习Python数据分析、自然语言处理（NLP）的初学者，以及对中国文学有兴趣的数据爱好者。

## 功能概述

- **词频统计**：通过使用jieba分词库，对《红楼梦》文本进行精确分词。
- **停用词过滤**：剔除常见停用词，专注于有意义的词汇分析。
- **个性化处理**：对特定词汇进行合并（如将不同称呼统一），增强分析的准确性。
- **词云生成**：采用wordcloud库，根据统计结果生成视觉化的词云图，展示高频词汇。
- **字体配置**：支持中文显示，需指定正确的中文字体文件路径（如simhei.ttf）。
- **代码示例**：提供了详细的代码段，涵盖了从读取文本、分词、统计词频到生成词云的全过程。

## 快速入门

1. **准备材料**：确保拥有《红楼梦.txt》文本文件和包含停用词的`stop_words.txt`。
2. **环境需求**：安装必要的Python库，包括`jieba`, `wordcloud`, 和 `matplotlib`。
3. **执行步骤**：
    - 导入所需模块。
    - 加载文本和停用词列表。
    - 应用分词，并根据规则清理词频数据。
    - 设置词云样式，包括字体、尺寸等。
    - 生成并显示词云图像。

## 示例代码片段

```python
import jieba
from wordcloud import WordCloud
import matplotlib.pyplot as plt

def wordFreq(filepath, text, topn):
    # 分词与初步处理
    words = jieba.lcut(text.strip())
    stopwords = [line.strip() for line in open('stop_words.txt', 'r', encoding='utf-8').readlines()]
    # 统计并返回处理后的词列表
    ...

def gen_cloudword(txt):
    # 初始化词云
    wcloud = WordCloud(font_path='simhei.ttf', width=1000, height=860)
    wcloud.generate(txt)
    # 保存并显示词云
    wcloud.to_file("红楼梦cloud.png")
    plt.imshow(wcloud)
    plt.axis('off')
    plt.show()
    
# 主流程
if __name__ == "__main__":
    with open('红楼梦.txt', 'r', encoding='utf-8') as f:
        text = f.read()
    words_clear = wordFreq('红楼梦.txt', text, 10)
    gen_cloudword(' '.join(words_clear))
```

## 注意事项

- 确保所有必需的文件（文本、停用词列表及中文字体文件）位于正确的位置。
- 根据实际环境调整字体路径。
- 分析结果受文本处理逻辑的影响，可适当调整以适应不同需求。

开始您的《红楼梦》数据探索之旅，发现隐藏在文字间的秘密吧！

## 下载链接

[Python之红楼梦词频统计并生成图云](https://pan.quark.cn/s/6a0be8496430)