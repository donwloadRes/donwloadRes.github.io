---
layout: post
title: "Stable Diffusion文生图模型训练入门实战完整代码
date   20200826
tags 训练文生模型model
comments true
author admin

 Stable Diffusion文生图模型训练入门实战完整代码

 简介

本资源文件提供了Stable Diffusion文生图模型训练的完整代码适合初学者入门实战Stable Diffusion 15SD15是由Stability AI在2022年8月22日开源的文生图模型是SD最经典也是社区最活跃的模型之一通过本资源您可以在火影忍者数据集上微调一个火影风格的文生图模型非Lora方式是学习SD训练的入门任务

 环境要求

 Python  38
 至少一张英伟达显卡显存大约要求22GB左右

 安装依赖

在您的计算机上安装以下Python库

bash
pip install swanlab diffusers datasets accelerate torchvision transformers


 数据集准备

本案例使用的是火影忍者数据集该数据集主要被用于训练文生图模型数据集由1200条图像描述对组成左边是火影人物的图像右边是对它的描述数据集的大小大约700MB左右

 模型准备

本案例使用HuggingFace上Runway发布的stablediffusionv15模型

 训练可视化工具

使用SwanLab来监控整个训练过程并评估最终的模型效果

 开始训练

训练代码较长请参考提供的代码文件进行训练训练参数如下

bash
python trainsd15narutopy 
  useema 
  resolution512 
  centercrop 
  randomflip 
  trainbatchsize1 
  gradientaccumulationsteps4 
  gradientcheckpointing 
  maxtrainsteps15000 
  learningrate1e05 
  maxgradnorm1 
  seed42 
  lrschedulerconstant 
  lrwarmupsteps0 
  outputdirsdnarutomodel


 训练结果演示

训练完成后您可以在SwanLab上查看最终的训练结果训练过程中loss会一直在震荡但随着epoch的增加loss在最初下降后后续的变化其实并不大

 模型推理

训练好的模型会放到sdnarutomodel文件夹下推理代码如下

python
from diffusers import StableDiffusionPipeline
import torch

modelid  sdnarutomodel
pipe  StableDiffusionPipelinefrompretrainedmodelid torchdtypetorchfloat16
pipe  pipetocuda

prompt  Lebron James with a hat"
date:   2020-08-26
tags: [--,训练,文生,模型,model]
comments: true
author: admin
---
# Stable Diffusion文生图模型训练入门实战（完整代码）

## 简介

本资源文件提供了Stable Diffusion文生图模型训练的完整代码，适合初学者入门实战。Stable Diffusion 1.5（SD1.5）是由Stability AI在2022年8月22日开源的文生图模型，是SD最经典也是社区最活跃的模型之一。通过本资源，您可以在火影忍者数据集上微调一个火影风格的文生图模型（非Lora方式），是学习SD训练的入门任务。

## 环境要求

- Python >= 3.8
- 至少一张英伟达显卡（显存大约要求22GB左右）

## 安装依赖

在您的计算机上安装以下Python库：

```bash
pip install swanlab diffusers datasets accelerate torchvision transformers
```

## 数据集准备

本案例使用的是火影忍者数据集，该数据集主要被用于训练文生图模型。数据集由1200条（图像、描述）对组成，左边是火影人物的图像，右边是对它的描述。数据集的大小大约700MB左右。

## 模型准备

本案例使用HuggingFace上Runway发布的stable-diffusion-v1-5模型。

## 训练可视化工具

使用SwanLab来监控整个训练过程，并评估最终的模型效果。

## 开始训练

训练代码较长，请参考提供的代码文件进行训练。训练参数如下：

```bash
python train_sd1-5_naruto.py \
  --use_ema \
  --resolution=512 \
  --center_crop \
  --random_flip \
  --train_batch_size=1 \
  --gradient_accumulation_steps=4 \
  --gradient_checkpointing \
  --max_train_steps=15000 \
  --learning_rate=1e-05 \
  --max_grad_norm=1 \
  --seed=42 \
  --lr_scheduler="constant" \
  --lr_warmup_steps=0 \
  --output_dir="sd-naruto-model"
```

## 训练结果演示

训练完成后，您可以在SwanLab上查看最终的训练结果。训练过程中，loss会一直在震荡，但随着epoch的增加，loss在最初下降后，后续的变化其实并不大。

## 模型推理

训练好的模型会放到sd-naruto-model文件夹下，推理代码如下：

```python
from diffusers import StableDiffusionPipeline
import torch

model_id = "/sd-naruto-model"
pipe = StableDiffusionPipeline.from_pretrained(model_id, torch_dtype=torch.float16)
pipe = pipe.to("cuda")

prompt = "Lebron James with a hat"
image = pipe(prompt).images[0]
image.save("result.png")
```

## 相关资源

- 代码文件：请参考提供的代码文件
- 实验日志过程：请参考提供的实验日志文件

## 作者

林泽毅

## 版权声明

本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[StableDiffusion文生图模型训练入门实战完整代码](https://pan.quark.cn/s/1970d3f05bb8)