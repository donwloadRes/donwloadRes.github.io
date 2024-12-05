---
layout: post
title: "中南大学毕业设计论文LaTeX模板"
date:   2024-08-05
tags: [模板,LaTeX,中南大学,毕业设计,论文]
comments: true
author: admin
---
# 中南大学毕业设计（论文）LaTeX模板

## 项目简介

本项目提供了一个完全依照中南大学本科生院发布的毕业设计（论文）Word模板格式制作的LaTeX模板。该模板旨在方便使用LaTeX编辑和排版论文的同学，所有环境命令均已调试合格，可直接下载使用。

## 项目特点

- **完全依照原Word模板格式**：模板严格按照中南大学本科生院发布的毕业设计（论文）Word模板格式制作，确保排版的一致性和规范性。
- **环境命令调试合格**：所有常见使用到的环境（目录、交叉引用和文献格式等）均已调试合格，用户可直接下载使用。
- **详细说明文档**：项目中的PDF文档对论文中常见使用到的环境进行了进一步的详细说明，帮助用户更好地理解和使用模板。

## 使用说明

1. **下载链接**：
   - GitHub: [LaTeX-Template-for-the-Undergraduate-Thesis-of-Central-South-University](https://github.com/xtChai/LaTeX-Template-for-the-Undergraduate-Thesis-of-Central-South-University)
   - 云盘：[百度云盘下载](https://pan.baidu.com/s/1LOLG7cnqPFJAwHjLsPvKPg) 提取码：82ku

2. **安装与使用**：
   - 下载模板文件后，解压缩并按照说明文档中的步骤进行安装和使用。
   - 模板文件中包含了详细的说明文档，用户可根据文档中的指导进行操作。

3. **取消参考文献后面的页码超链接**：
   - 在“THSIS_csu.tex”文件中，删除第5行中括号中的“backref=page”命令：
     ```latex
     \usepackage[pdftex,linkcolor=blue,citecolor=blue,backref=page,hyperfootnotes=false]{hyperref}
     ```
     替换为：
     ```latex
     \usepackage[pdftex,linkcolor=blue,citecolor=blue,hyperfootnotes=false]{hyperref}
     ```

## 作者信息

- 作者：Chai Xingtao
- 邮箱：xtChai@yeah.net

## 版权声明

本模板为原创作品，遵循 CC 4.0 BY-SA 版权协议。转载请附上原文出处链接和本声明。

## 致谢

感谢中南大学本科生院提供的毕业设计（论文）Word模板，为本项目的制作提供了基础。

## 下载链接

[中南大学毕业设计论文LaTeX模板分享](https://pan.quark.cn/s/00ae5d18afd0)