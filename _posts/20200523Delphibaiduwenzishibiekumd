---
layout: post
title: "Delphi百度文字识别库"
date:   2024-09-14
tags: [识别,API,Delphi,文字,Key]
comments: true
author: admin
---
# Delphi百度文字识别库

## 简介

本开源仓库提供了一个Delphi库，用于集成百度文字识别API。该库支持多种文字识别功能，涵盖了从通用文字识别到特定证件和票据的识别，适用于Delphi 7到XE10的版本。

## 功能列表

本库支持以下文字识别功能：

- 通用文字识别
- 通用文字识别（高精度版）
- 通用文字识别（含位置信息版）
- 通用文字识别（高精度含位置版）
- 手写文字识别
- 身份证识别
- 银行卡识别
- 营业执照识别
- 护照识别
- 名片识别
- 户口本识别
- 出生医学证明识别
- 港澳通行证识别
- 台湾通行证识别
- 表格文字识别
- 通用票据识别
- 增值税发票识别
- 火车票识别
- 出租车票识别
- 定额发票识别
- 驾驶证识别
- 行驶证识别
- 车牌识别
- 机动车销售发票识别
- 车辆合格证识别
- VIN码识别
- 二维码识别
- 数字识别
- 网络图片文字识别
- 彩票识别
- 保单识别
- 通用机打发票识别
- 行程单识别

## 使用说明

1. **获取百度API密钥**：
   - 访问[百度AI开放平台](https://ai.baidu.com/)，注册并创建一个应用，获取API Key和Secret Key。

2. **集成库文件**：
   - 将本仓库中的Delphi库文件集成到您的项目中。

3. **配置API密钥**：
   - 在您的Delphi项目中配置百度API的API Key和Secret Key。

4. **调用识别功能**：
   - 根据您的需求调用相应的识别功能，传入图片路径或图片数据，获取识别结果。

## 示例代码

以下是一个简单的示例代码，展示如何使用本库进行身份证识别：

```delphi
uses
  BaiduOCR;

procedure TForm1.Button1Click(Sender: TObject);
var
  OCR: TBaiduOCR;
  Result: string;
begin
  OCR := TBaiduOCR.Create('您的API Key', '您的Secret Key');
  try
    Result := OCR.RecognizeIDCard('path/to/idcard.jpg');
    ShowMessage(Result);
  finally
    OCR.Free;
  end;
end;
```

## 依赖

- Delphi 7 及以上版本
- 百度AI开放平台API密钥

## 贡献

欢迎提交Issue和Pull Request，共同完善本库。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[Delphi百度文字识别库](https://pan.quark.cn/s/c0bb3fad993c)