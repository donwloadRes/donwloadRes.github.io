---
layout: post
title: "医保电子凭证二维码识别 - NationECCode.dll"
date:   2024-12-04
tags: [医保,凭证,二维码,电子,NationECCode]
comments: true
author: admin
---
# 医保电子凭证二维码识别 - NationECCode.dll

## 概述

本仓库提供了`NationECCode.dll`，一个专门用于识别医保电子凭证二维码的国家医保电子凭证业务标准动态库。此外，还包括`NationECCodeTest.exe`，作为一个示例程序，帮助开发者理解和应用这个动态库的交互规范。通过本资源，开发者可以轻松集成医保电子凭证的二维码识别功能到其应用程序中，遵循2021年更新的业务标准和交互规范。

## 功能特点

- **高效识别**: 支持快速准确地解码医保电子凭证上的二维码信息。
- **标准兼容**: 完全符合国家医保局发布的电子凭证业务标准。
- **环境适应性强**: 提供了测试、预发和生产三个不同环境的查询地址，覆盖开发至上线全周期。
- **示例代码**: 随库附带测试工具`NationECCodeTest.exe`，包含基本用法，方便快速上手。

## 技术文档及环境

- **接口说明**：资源包内包含2021年12月23日更新的医保电子凭证测试说明，详细解释了如何使用此动态库进行二维码解码操作。
- **请求地址**：
  - **测试环境**：http://10.249.84.44:8089/localcfc/api/hsecfc/localQrCodeQuery
  - **预发环境**：http://10.249.83.229/localcfc/api/hsecfc/localQrCodeQuery
  - **生产环境**：http://10.249.81.107/localcfc/api/hsecfc/localQrCodeQuery

- **请求样例**:
  ```json
  {
    "data": {
      "orgId": "H46010500002",
      "businessType": "01101",
      "operatorId": "test001",
      "operatorName": "超级管理员",
      "officeId": "32760",
      "officeName": "消化内科"
    }
  }
  ```

## 使用步骤

1. 将`NationECCode.dll`添加到你的项目引用中。
2. 引入必要的命名空间，并参照提供的示例代码进行调用。
3. 根据实际需求，配置正确的环境地址进行数据交换。
4. 实现医保电子凭证二维码的识别逻辑。

## 注意事项

- 在正式部署前，请确保在测试环境下充分验证应用功能。
- 确保所有数据传输遵守国家医保局的相关规定和隐私政策。

## 开源贡献

欢迎社区成员提出问题、建议或贡献代码改进。请通过提交GitHub issue或者Pull Request参与进来。

---

通过本仓库，我们希望促进医疗信息化的发展，简化医保电子凭证的集成过程，期待您的积极参与！

## 下载链接

[医保电子凭证二维码识别-NationECCode.dll](https://pan.quark.cn/s/68e0ffa128e5)