---
layout: post
title: "JS AES加密解密实现"
date:   2021-01-21
tags: [CryptoJS,加密,AES,解密,text]
comments: true
author: admin
---
# JS AES加密解密实现

## 简介
本仓库提供了一个用于JavaScript的AES加密解密实现的资源文件。该资源文件基于CryptoJS库，支持AES加密和解密操作，适用于前端开发中的数据加密需求。

## 功能特点
- **AES CBC模式**：支持AES加密解密的CBC模式。
- **AES ECB模式**：支持AES加密解密的ECB模式。
- **简单易用**：提供了加密和解密的函数，方便开发者直接调用。

## 使用方法
1. 引入CryptoJS库。
2. 调用提供的加密和解密函数，传入相应的参数即可完成加密和解密操作。

## 示例代码
以下是使用AES CBC模式进行加密和解密的示例代码：

```javascript
<script type="text/javascript" src="crypto-js.js"></script>
<script type="text/javascript">
    const key = '235325fdgerteGHdsfsdewred4345341'; // 32位
    const iv = '4387438hfdhfdjhg'; // 16位
    const txt = '我们是不是实现加密了 哈哈哈哈';

    // 加密
    function encrypt(text) {
        return CryptoJS.AES.encrypt(text, CryptoJS.enc.Utf8.parse(key), {
            iv: CryptoJS.enc.Utf8.parse(iv),
            mode: CryptoJS.mode.CBC,
            padding: CryptoJS.pad.Pkcs7
        }).toString();
    }

    // 解密
    function decrypt(text) {
        let decrypted = CryptoJS.AES.decrypt(text, CryptoJS.enc.Utf8.parse(key), {
            iv: CryptoJS.enc.Utf8.parse(iv),
            mode: CryptoJS.mode.CBC,
            padding: CryptoJS.pad.Pkcs7
        });
        return decrypted.toString(CryptoJS.enc.Utf8);
    }

    const sign = encrypt(txt);
    console.log('加密：', sign);
    const _src = decrypt(sign);
    console.log('解密：', _src);
</script>
```

## 注意事项
- 密钥和初始向量（IV）的长度必须符合AES算法的要求。
- 加密和解密过程中使用的密钥和IV必须一致。

## 贡献
欢迎提交Issue和Pull Request，共同完善本资源文件。

## 许可证
本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[JSAES加密解密实现](https://pan.quark.cn/s/5214a628b1fd)