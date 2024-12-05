---
layout: post
title: "tesseract未安装或不在PATH环境变量中的解决办法"
date:   2021-11-17
tags: [安装,pytesseract,Tesseract,环境变量,tesseract]
comments: true
author: admin
---
# tesseract未安装或不在PATH环境变量中的解决办法

当您在尝试使用Python的`pytesseract`库进行文本识别时，可能会遇到错误提示：“tesseract is not installed or it’s not in your PATH”。这个问题表明您的系统尚未安装Tesseract OCR引擎，或者安装了但Python无法找到其路径。本资源提供了详细的解决步骤，确保您可以顺利地使用`pytesseract`。

## 安装Tesseract OCR

1. **下载与安装**  
   首先，访问[Tesseract OCR GitHub页面](https://github.com/UB-Mannheim/tesseract)下载适合您操作系统的安装包，并按照指示完成安装。对于Windows用户，安装过程中记得勾选“添加到系统路径”选项，这样Tesseract就会自动添加到环境变量中。

2. **使用Anaconda或pip安装pytesseract**  
   在命令行中输入`pip install pytesseract`来安装`pytesseract`库。如果您使用的是Anaconda环境，同样可以通过conda命令进行安装。

## 手动配置环境变量

如果安装过程中未自动添加到PATH，或您是从GitHub或其他途径下载的手动安装包，需手动配置：

1. **查找Tesseract的可执行文件路径**，通常位于安装目录下的`bin`文件夹。
2. **添加到系统环境变量**：进入系统设置，找到环境变量，在“系统变量”的`Path`中添加上述路径。

## 中文支持与额外包安装

对于需要中文识别的情况，您可能需要下载并安装中文语言包。这可以通过访问特定资源或直接从Tesseract的GitHub页面找到相关的语言数据文件来进行。

## 验证安装

安装并配置完毕后，通过运行简单的Python脚本来验证是否一切就绪：

```python
import pytesseract
from PIL import Image

image_path = 'path_to_your_image.png' # 图像文件路径
text = pytesseract.image_to_string(Image.open(image_path))
print(text)
```

如果这段代码能够成功打印出图片中的文本而没有抛出"TesseractNotFoundError"，那么说明您的问题已经成功解决。

记住，良好的开发习惯包括确认所有依赖项均正确安装并配置，这对于避免此类问题至关重要。希望这些步骤能帮助您快速解决问题，愉快地使用Tesseract进行文本识别。

## 下载链接

[tesseract未安装或不在PATH环境变量中的解决办法](https://pan.quark.cn/s/00ba616d5722)