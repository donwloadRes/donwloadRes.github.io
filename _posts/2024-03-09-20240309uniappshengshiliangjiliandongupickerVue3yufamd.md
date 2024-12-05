---
layout: post
title: "uniapp 省市两级联动 upicker Vue3语法"
date:   2024-02-20
tags: [const,value,picker,uniapp,ref]
comments: true
author: admin
---
# uniapp 省市两级联动 u-picker (Vue3语法)

## 简介
本资源文件提供了一个基于Vue3语法的uniapp省市两级联动组件，使用u-picker插件实现。该组件可以帮助开发者在uniapp项目中快速实现省市两级联动的功能。

## 功能特点
- **省市两级联动**：支持省和市的两级联动选择。
- **Vue3语法**：完全兼容Vue3语法，适用于最新的uniapp项目。
- **数据源灵活**：支持自定义数据源，方便集成到不同的项目中。

## 使用方法
1. **引入插件**：
    ```vue
    <u-picker :show="show" ref="uPicker" :columns="newList" @confirm="confirm" @change="changeHandler" @cancel="cancel" itemHeight="80"></u-picker>
    ```

2. **数据源配置**：
    ```javascript
    import jsonData from '@/utils/pc.json'; // 所有的地图数据
    const addressData = ref([]);
    addressData.value = jsonData;
    const cityName = ref(); // 记录市的字段
    const provinceName = ref('请选择城市'); // 记录省的字段
    const newList = ref([]); // 绑定控件数据源的字段
    ```

3. **页面加载时调用**：
    ```javascript
    onLoad((name) => {
        // 省的数据
        const provinceData = jsonData.map(e => { return e.name });
        // 市的数据
        const cityData = jsonData.map(e => {
            const arr = [];
            arr.push(e.children.map(c => { return c.name }));
            return arr;
        });
        const arr = [provinceData, cityData[0][0]]; // 数据的初始数据
        newList.value = arr;
    });
    ```

4. **点击确定按钮时的逻辑**：
    ```javascript
    const confirm = (e) => {
        province.value = e.value[0];
        city.value = e.value[1];
        show.value = false;
    };
    ```

5. **选择地址时的数据响应**：
    ```javascript
    const changeHandler = (e) => {
        const [columnIndex, value, values, index, picker] = e;
        if (columnIndex === 0) {
            if (!isNaN(index)) {
                const children1 = addressData.value[index].children.map(e => { return e.name });
                picker.setColumnValues(1, children1);
            }
        }
    };
    ```

6. **关闭窗口的方法**：
    ```javascript
    const cancel = () => {
        show.value = false;
        isRotated.value = false;
    };
    ```

## 注意事项
- 确保项目中已经安装并配置了u-picker插件。
- 数据源文件`pc.json`需要根据实际需求进行调整。

## 贡献
欢迎提交PR或Issue，帮助改进和完善该组件。

## 许可证
本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[uniapp省市两级联动u-pickerVue3语法](https://pan.quark.cn/s/4a5d092dc81f)