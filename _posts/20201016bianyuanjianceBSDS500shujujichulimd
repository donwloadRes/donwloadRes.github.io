---
layout: post
title: "边缘检测BSDS500数据集处理"
date:   2024-04-12
tags: [os,sub,data,pth,name]
comments: true
author: admin
---
# 边缘检测BSDS500数据集处理

## 简介
本资源文件提供了边缘检测BSDS500数据集的处理方法和相关代码。BSDS500数据集是一个广泛用于图像分割和轮廓检测的数据集，包含200张训练图像、200张测试图像和100张验证图像。数据集的标签以`.mat`格式保存，需要转换为常见的图像格式（如`.jpg`或`.png`）以便于网络训练。

## 数据集处理步骤
1. **数据集下载**：从官方网站下载BSDS500数据集。
2. **标签格式转换**：将`.mat`格式的标签文件转换为`.jpg`或`.png`格式。
3. **图像叠加**：将不同标注者标注的标签进行图像叠加，生成最终的标签图像。

## 代码示例
以下是数据集处理的核心代码示例，展示了如何读取`.mat`文件并将其转换为图像格式：

```python
from scipy import io
import imageio
import os

def bsds_trans(root, num_anno):
    PATH = os.path.join(root, 'data\\groundTruth')
    for sub_dir_name in ['train', 'test', 'val']:
        sub_pth = os.path.join(PATH, sub_dir_name)
        save_pth = os.path.join(root, 'data\\GT_convert_{}'.format(num_anno), sub_dir_name)
        os.makedirs(save_pth, exist_ok=True)
        print('开始转换' + sub_dir_name + '文件夹中内容')
        for index in range(len(os.listdir(sub_pth))):
            filename = os.listdir(sub_pth)[index]
            data = io.loadmat(os.path.join(sub_pth, filename))
            try:
                if len(data['groundTruth'][0]) < num_anno + 1:
                    raise IndexError
                edge_data = data['groundTruth'][0][num_anno][0][0][1]
                edge_data_255 = edge_data * 255
                new_img_name = filename.split('.')[0] + '.jpg'
                print(new_img_name)
                imageio.imsave(os.path.join(save_pth, new_img_name), edge_data_255)
            except IndexError:
                index = min(len(os.listdir(sub_pth)) - 1, index + 1)
                filename = os.listdir(sub_pth)[index]

if __name__ == '__main__':
    root = 'D:\\桌面\\bsds500\\BSR\\BSDS500'
    num_anno = 5
    bsds_trans(root, num_anno)
```

## 注意事项
1. **标注者选择**：数据集由多个标注者完成，可以通过更改`num_anno`参数选择不同标注者的标签。
2. **异常处理**：部分标注者可能未标注所有图像，代码中已添加异常处理机制。
3. **图像叠加**：处理后的标签图像可以进行叠加，以生成更丰富的训练数据。

## 参考
本资源文件的处理方法参考了CSDN博客文章《边缘检测BSDS500数据集处理》，详细内容可查阅该文章。

## 贡献
欢迎对本资源文件进行改进和优化，提交Pull Request或Issue。

## 许可证
本资源文件遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[边缘检测BSDS500数据集处理](https://pan.quark.cn/s/55ab78671ced)