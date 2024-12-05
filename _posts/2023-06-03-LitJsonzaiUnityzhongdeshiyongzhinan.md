---
layout: post
title: "LitJson在Unity中的使用指南"
date:   2023-05-24
tags: [JSON,Unity,JsonData,LitJson,string]
comments: true
author: admin
---
# LitJson在Unity中的使用指南

## 简介
LitJson是一个轻量级的JSON库，广泛应用于Unity游戏开发中，用于处理JSON数据的序列化和反序列化。本资源文件提供了LitJson在Unity中的详细使用方法，帮助开发者高效地处理JSON数据。

## 主要内容

### 1. LitJson的导入
- 将LitJson的DLL文件放入Unity项目的`Assets/Plugins`文件夹中。
- 如果没有`Plugins`文件夹，请自行创建。

### 2. LitJson API介绍
- **JsonData**: 中转格式，表示一个对象，便于对JSON进行读取、写入和生成操作。
- **JsonMapper.ToJson()**: 将任何格式转化为JSON字符串。
- **JsonMapper.ToObject<T>(string)**: 将JSON字符串转化为任意T格式。

### 3. 获取和生成JSON示例
- **获取JSON文件**: 从Unity的`streamingAssets`文件夹中读取JSON文件，并将其转化为JsonData格式。
- **生成JSON文件**: 使用JsonData或JsonMapper和类生成JSON文件。

### 4. 示例代码
- **读取JSON文件**:
  ```csharp
  public JsonData jsonData;
  void LoadJson() {
      string configPath = Application.streamingAssetsPath + "/JsonStudyConfig.json";
      if (!File.Exists(configPath)) {
          Debug.LogError("严重错误，配置文件不存在");
      }
      string _config = File.ReadAllText(configPath);
      jsonData = JsonMapper.ToObject<JsonData>(_config);
  }
  ```

- **生成JSON文件**:
  ```csharp
  void WriteJson() {
      JsonData wJsonData = new JsonData();
      wJsonData["FoodName"] = "西红柿炒鸡蛋";
      wJsonData["FoodNum"] = 4;
      string json = wJsonData.ToJson();
      string path = Application.streamingAssetsPath + "/myJson.json";
      StreamWriter sw = new StreamWriter(path);
      sw.Write(json);
      sw.Close();
      sw.Dispose();
  }
  ```

## 注意事项
- JSON中使用`[]`表示数组结构，使用`{}`表示对象结构。
- “键”：“值”的方式表示属性及值。

## 总结
通过本资源文件，开发者可以快速掌握LitJson在Unity中的使用方法，高效处理JSON数据，提升开发效率。

## 下载链接

[LitJson在Unity中的使用指南分享](https://pan.quark.cn/s/68422b27e3bd)