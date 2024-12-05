---
layout: post
title: "128位AES加密资源C语言实现"
date:   2021-04-03
tags: [txt,加密,解密,AES,文件]
comments: true
author: admin
---
## 128位AES加密资源C语言实现

## 项目概述

本资源提供了使用C语言实现的128位AES加密算法。此实现采用Java原生态接口（JNI），适用于需要在Java环境中使用AES加密的场景。代码包含AES加密的核心实现，包括密钥生成、加密和解密过程。此外，还提供文件加密和解密接口，方便对文件进行直接操作。

## 功能特性

- **AES加密算法实现**：支持128位AES加密，涵盖加密和解密功能。
- **JNI兼容性**：代码可供Java的JNI调用，便于Java开发者集成。
- **文件加密/解密接口**：支持对文件进行加密和解密操作。

## 代码结构

- **密钥生成函数**：生成AES密钥。
- **置换函数**：执行初始置换、密钥置换和扩展置换等操作。
- **S盒函数**：应用S盒替换。
- **加密/解密函数**：执行分组加密和解密。
- **文件加密/解密函数**：提供对文件进行加密和解密的接口。

## 使用指南

### 编译

1. 将代码保存为`.c`文件。
2. 使用C编译器（如GCC）进行编译：

```bash
gcc -o aes_encrypt aes_encrypt.c
```

### 运行

**加密文件**：

```bash
./aes_encrypt 1.txt key.txt 2.txt
```

* `1.txt`：待加密文件
* `key.txt`：AES密钥文件（16字节）
* `2.txt`：加密后输出文件

**解密文件**：

```bash
./aes_encrypt 2.txt key.txt 3.txt
```

* `2.txt`：待解密文件
* `key.txt`：用于加密的AES密钥文件
* `3.txt`：解密后输出文件

### 示例代码

```c
int main() {
    DES_Encrypt("1.txt", "key.txt", "2.txt");
    DES_Decrypt("2.txt", "key.txt", "3.txt");
    return 0;
}
```

## 注意事项

- AES密钥必须为长度为16字节的有效值。
- 文件字节数必须是8的倍数。

## 贡献

欢迎对该资源进行改进和优化。如果您有任何建议或发现错误，请提交Issue或Pull Request。

## 许可证

本资源采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[128位AES加密算法C语言实现](https://pan.quark.cn/s/56f62656bd9c)