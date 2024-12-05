---
layout: post
title: "Mann-Kendall趋势检验和突变点分析Matlab版程序"
date:   2020-12-01
tags: [程序,Mann,Kendall,mkabrpt,smk]
comments: true
author: admin
---
# Mann-Kendall趋势检验和突变点分析Matlab版程序

本仓库提供了一个用于Mann-Kendall趋势检验和突变点分析的Matlab程序资源文件。该资源文件包含两个主要程序：`mk` 和 `mkabrpt`，以及辅助程序 `smk`。以下是详细介绍：

## 资源文件内容

1. **mk**：
   - 这是一个Mann-Kendall趋势性检验程序。
   - 该程序由他人编写，未考虑序列中相等的值（即“结”）。
   - 适用于对时间序列数据进行趋势性检验。

2. **mkabrpt**：
   - 这是一个Mann-Kendall突变点分析的程序。
   - 该程序会调用 `smk` 程序来计算秩。
   - 由本人编写，适用于对时间序列数据进行突变点分析。

3. **smk**：
   - 这是一个辅助程序，用于计算秩。
   - 由 `mkabrpt` 程序调用。

## 使用说明

- 每个程序的头部都有简单的参数说明，方便用户快速了解程序的使用方法。
- 仓库内还包含一个 `readme.txt` 文件，提供了更详细的使用说明和注意事项。

## 注意事项

- `mk` 程序未考虑序列中的“结”，即相等的值，用户在使用时需注意这一点。
- `mkabrpt` 程序依赖于 `smk` 程序，确保在运行 `mkabrpt` 时，`smk` 程序也在同一目录下。

希望这个资源文件能帮助您在Matlab中进行Mann-Kendall趋势检验和突变点分析。如有任何问题或建议，欢迎反馈！

## 下载链接

[Mann-Kendall趋势检验和突变点分析Matlab版程序](https://pan.quark.cn/s/53eb31a4ff1d)