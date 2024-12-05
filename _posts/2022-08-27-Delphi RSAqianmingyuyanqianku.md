---
layout: post
title: "Delphi RSA签名与验签库"
date:   2021-01-29
tags: [Delphi,与验,签名,your,秘钥]
comments: true
author: admin
---
# Delphi RSA签名与验签库

## 简介
本开源仓库提供了一个Delphi库，用于实现RSA签名与验签功能。该库支持三种签名与验签方式（SHA1WithRSA、SHA256WithRSA和MD5WithRSA），并且支持PKCS8和PKCS1两种秘钥格式。此外，还提供了UTF-8和GBK两种字符集选择，兼容Delphi 7到Delphi XE10版本。

## 功能特点
- **支持的签名与验签方式**：
  - SHA1WithRSA
  - SHA256WithRSA
  - MD5WithRSA
- **支持的秘钥格式**：
  - PKCS8
  - PKCS1
- **支持的字符集**：
  - UTF-8
  - GBK
- **兼容性**：
  - Delphi 7
  - Delphi 2007
  - Delphi 2009
  - Delphi 2010
  - Delphi XE
  - Delphi XE2
  - Delphi XE3
  - Delphi XE4
  - Delphi XE5
  - Delphi XE6
  - Delphi XE7
  - Delphi XE8
  - Delphi 10 Seattle
  - Delphi 10.1 Berlin
  - Delphi 10.2 Tokyo
  - Delphi 10.3 Rio
  - Delphi 10.4 Sydney

## 使用方法
1. **下载仓库**：
   ```bash
   git clone https://github.com/your-repo-url.git
   ```

2. **导入库文件**：
   将库文件导入到你的Delphi项目中。

3. **配置秘钥和字符集**：
   根据需要配置秘钥格式和字符集。

4. **调用签名与验签函数**：
   使用提供的函数进行RSA签名与验签操作。

## 示例代码
以下是一个简单的示例代码，展示了如何使用该库进行RSA签名与验签：

```delphi
uses
  RSAUtils;

procedure Example;
var
  PrivateKey, PublicKey, Data, Signature: string;
begin
  // 初始化秘钥和数据
  PrivateKey := 'your_private_key';
  PublicKey := 'your_public_key';
  Data := 'data_to_sign';

  // 进行签名
  Signature := RSAUtils.SignData(Data, PrivateKey, SHA256WithRSA, UTF8);

  // 进行验签
  if RSAUtils.VerifySignature(Data, Signature, PublicKey, SHA256WithRSA, UTF8) then
    ShowMessage('验签成功')
  else
    ShowMessage('验签失败');
end;
```

## 贡献
欢迎大家贡献代码，提出问题和建议。请通过GitHub的Issue和Pull Request功能进行交流。

## 许可证
本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 联系方式
如有任何问题，请联系项目维护者：
- 邮箱：your-email@example.com
- GitHub：[your-github-username](https://github.com/your-github-username)

---
感谢使用本库，希望它能帮助你顺利完成项目开发！

## 下载链接

[DelphiRSA签名与验签库](https://pan.quark.cn/s/2d8be017910c)