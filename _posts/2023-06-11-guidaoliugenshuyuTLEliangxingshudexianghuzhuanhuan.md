---
layout: post
title: "轨道六根数与TLE两行数的相互转换"
date:   2023-09-29
tags: [TLE,六根,let,轨道,Number]
comments: true
author: admin
---
# 轨道六根数与TLE两行数的相互转换

本仓库提供了一个使用JavaScript语言编写的工具，用于实现轨道六根数（COE - Classical Orbital Elements）与TLE（Two-Line Element set）两行数的相互转换。代码中包含了详细的注释，解释了转换过程中的每一步，使得理解和使用变得简单易懂。

## 功能描述

- **TLE转轨道六根数**：将TLE两行数转换为轨道六根数。
- **轨道六根数转TLE**：将轨道六根数转换为TLE两行数。

## 使用方法

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo-url.git
   ```

2. **引入文件**：
   将仓库中的JavaScript文件引入到你的项目中。

3. **调用函数**：
   - 将TLE两行数转换为轨道六根数：
     ```javascript
     let TLE = {
       tle1: "1 25544U 98067A   21275.56782528  .00005714  00000-0  11277-3 0  9994",
       tle2: "2 25544  51.6444 236.2121 0003794  92.7660 267.3979 15.49248265300695"
     };
     let COE = TLE2COE(TLE);
     console.log(COE);
     ```

   - 将轨道六根数转换为TLE两行数：
     ```javascript
     let COE = {
       epochYear: 2021,
       epochDay: 275.56782528,
       elementI: 51.6444,
       elementO: 236.2121,
       elementE: 0.0003794,
       elementW: 92.7660,
       // 其他轨道六根数参数
     };
     let TLE = COE2TLE(COE);
     console.log(TLE);
     ```

## 代码示例

以下是部分代码示例，展示了如何从TLE两行数中提取轨道六根数：

```javascript
function TLE2COE(TLE) {
    let epochYear = Number(TLE.tle1.substr(18, 2));
    let epochDay = Number(TLE.tle1.substr(20, 12));
    let epochTime = getEpoch(epochYear, epochDay);
    // 倾角
    let elementI = Number(TLE.tle2.substr(8, 8));
    // 升交点赤经
    let elementO = Number(TLE.tle2.substr(17, 8));
    // 偏心率
    let elementE = Number('0.' + TLE.tle2.substr(26, 7));
    // 近地点幅角
    let elementW = Number(TLE.tle2.substr(34, 8));
    // 其他轨道六根数参数
    // ...

    return {
        epochYear,
        epochDay,
        elementI,
        elementO,
        elementE,
        elementW,
        // 其他轨道六根数参数
    };
}
```

## 贡献

欢迎贡献代码、提出问题或建议。请通过GitHub的Issue和Pull Request功能进行。

## 许可证

本项目采用[MIT许可证](LICENSE)。

## 下载链接

[轨道六根数与TLE两行数的相互转换](https://pan.quark.cn/s/1a570ba874c1)