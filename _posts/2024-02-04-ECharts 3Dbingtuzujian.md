---
layout: post
title: "ECharts 3D饼图组件"
date:   2023-02-26
tags: [组件,PieChart3D,name,value,color]
comments: true
author: admin
---
# ECharts 3D饼图组件

## 简介

本仓库提供了一个基于ECharts的3D饼图组件，方便开发者快速集成到项目中。该组件可以直接引入并传入数据即可使用，无需复杂的配置。

## 使用方法

1. **引入组件**：
   ```javascript
   import PieChart3D from '@/components/PieChart3D';
   ```

2. **传入数据**：
   ```javascript
   <PieChart3D
     values={[
       { name: '整租', value: 3, color: [5, 140, 198, 1] },
       { name: '散租', value: 2, color: [255, 137, 0, 1] }
     ]}
   />
   ```

## 参数说明

- `values`：饼图的数据数组，每个对象包含以下属性：
  - `name`：数据项的名称。
  - `value`：数据项的值。
  - `color`：数据项的颜色，格式为RGBA数组。

## 示例

以下是一个简单的示例，展示了如何使用该组件：

```javascript
import React from 'react';
import PieChart3D from '@/components/PieChart3D';

const App = () => {
  const data = [
    { name: '整租', value: 3, color: [5, 140, 198, 1] },
    { name: '散租', value: 2, color: [255, 137, 0, 1] }
  ];

  return (
    <div>
      <PieChart3D values={data} />
    </div>
  );
};

export default App;
```

## 注意事项

- 确保项目中已经安装了ECharts库。
- 该组件适用于React项目，其他框架可能需要进行适配。

## 贡献

欢迎提交PR或提出Issue，帮助改进该组件。

## 下载链接

[ECharts3D饼图组件](https://pan.quark.cn/s/278d126c83f6)