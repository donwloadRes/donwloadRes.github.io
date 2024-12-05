---
layout: post
title: "VantUI下拉搜索框实现方法基于Vue的教程
date   20220322
tags VueVantUIvanvalue搜索
comments true
author admin

 VantUI下拉搜索框实现方法基于Vue的教程

欢迎来到本教程我们将一起学习如何在Vue项目中集成一个具备搜索功能的下拉选择框使用流行的移动端UI框架VantUI如果你正寻找一个简易且高效的方式为你的移动应用增添这一实用功能那么你来对地方了

 示例概述

本文档指导你通过简单的步骤实现一个VantUI的下拉搜索框组件该组件结合了vanfield作为输入框和vanpicker作为选择器并通过自定义逻辑完成搜索过滤功能

 快速开始

 步骤 1  准备工作

确保你已安装了VantUI并正确配置在你的Vue项目中如果没有请访问VantUI官方文档httpsvantcontribgiteeiovantzhCN来了解如何开始

 步骤 2  HTML 结构

在你的Vue组件模板中添加以下结构

html
div
  vanfield
    label所属部门
    readonly
    clickable
    required
    placeholder点击选择所在部门
    clickshowPickertrue
    valuevalue
  
  vanpopup vmodelshowPicker positionbottom
    vanfield
      clickable
      vmodeltrimkeyvalue
      lefticonsearch
      placeholder搜索所在部门
      inputsearch
    
    vanpicker
      showtoolbar
      columnsfilterdepartments
      confirmonConfirm
      cancelshowPickerfalse"
date:   2022-03-22
tags: [Vue,VantUI,van,value,搜索]
comments: true
author: admin
---
# VantUI下拉搜索框实现方法基于Vue的教程

欢迎来到本教程，我们将一起学习如何在Vue项目中集成一个具备搜索功能的下拉选择框，使用流行的移动端UI框架VantUI。如果你正寻找一个简易且高效的方式为你的移动应用增添这一实用功能，那么你来对地方了。

## 示例概述

本文档指导你通过简单的步骤实现一个VantUI的下拉搜索框组件。该组件结合了`van-field`作为输入框和`van-picker`作为选择器，并通过自定义逻辑完成搜索过滤功能。

## 快速开始

### 步骤 1 - 准备工作

确保你已安装了VantUI并正确配置在你的Vue项目中。如果没有，请访问[VantUI官方文档](https://vant-contrib.gitee.io/vant/#/zh-CN/)来了解如何开始。

### 步骤 2 - HTML 结构

在你的Vue组件模板中添加以下结构：

```html
<div>
  <van-field
    label="所属部门"
    readonly
    clickable
    required
    placeholder="点击选择所在部门"
    @click="showPicker=true"
    :value="value"
  />
  <van-popup v-model="showPicker" position="bottom">
    <van-field
      clickable
      v-model.trim="keyvalue"
      left-icon="search"
      placeholder="搜索所在部门"
      @input="search"
    />
    <van-picker
      show-toolbar
      :columns="filterdepartments"
      @confirm="onConfirm"
      @cancel="showPicker=false"
    >
    </van-picker>
  </van-popup>
</div>
```

### 步骤 3 - 数据与方法

在组件的`data`选项中定义必要的数据属性，并在`methods`中实现搜索和选择的功能：

```javascript
new Vue({
  el: "#root",
  data() {
    return {
      value: "", // 选中项的值
      keyvalue: "", // 搜索关键词
      filterdepartments: null, // 过滤后的部门列表
      departments: [
        { text: "销售部", value: "XSB" },
        // ...其他部门数据
      ],
      showPicker: false,
    };
  },
  mounted() {
    // 初始化过滤数组为原始部门列表
    this.filterdepartments = this.departments;
  },
  methods: {
    search() {
      // 根据关键词过滤部门列表
      this.filterdepartments = this.departments.filter(dep =>
        dep.text.includes(this.keyvalue)
      );
    },
    onConfirm(value) {
      // 确认选择时的操作
      this.value = value.text;
      this.showPicker = false;
    },
  },
});
```

## 实现细节

- 用户点击“所属部门”触发显示弹出式下拉框。
- 输入框实时响应用户的输入，通过`search`方法动态筛选下拉列表。
- `onConfirm`方法处理用户的选择，更新父组件的数据并关闭弹出框。

## 结论

通过以上步骤，你将成功集成一个功能完备的下拉搜索框至你的Vue应用中，利用VantUI提供的组件和一些简单的自定义逻辑。这个小部件不仅增强了用户交互体验，也展示了Vue灵活的组件系统和VantUI的强大功能性。祝你在Vue开发旅程中取得更多成就！

## 下载链接

[VantUI下拉搜索框实现方法基于Vue的教程](https://pan.quark.cn/s/54b6bc2a8f18)