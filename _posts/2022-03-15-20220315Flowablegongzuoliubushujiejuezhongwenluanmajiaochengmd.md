---
layout: post
title: "Flowable工作流部署解决中文乱码教程"
date:   2024-07-13
tags: [字体,宋体,Flowable,流程图,中文]
comments: true
author: admin
---
# Flowable工作流部署解决中文乱码教程

## 概述

本文档为您提供了一份详细指南，帮助您解决在Flowable工作流部署到服务器后，生成流程图时遇到的中文乱码问题。适用于那些在Linux服务器环境下使用Flowable的企业和开发者，确保流程图中的中文能够正确显示。

## 步骤概览

1. **字体准备**: 确保拥有适合的中文字体包，如宋体。
2. **字体上传**: 将字体文件上传到服务器的 `/usr/share/fonts` 目录下。
3. **安装字体**: 在服务器上解压字体包，并使用 `fc-cache -fv` 命令安装。
4. **Flowable配置**: 更新Flowable配置以使用支持中文的字体。
5. **代码调整**: 确保生成流程图的代码中指定了正确的字体。
6. **服务重启**: 应用更改后重启相关Java服务。
7. **验证结果**: 访问流程图确认中文是否正常显示。

## 详细步骤

### 1. 获取字体包

首先，您可能需要从可靠的来源获取中文字体文件，如宋体字体。如果未持有，可寻找合法途径下载。

### 2. 上传及安装字体

- 将字体文件（例如 `.ttf` 文件）上传到 Linux 服务器的 `/usr/share/fonts` 目录。
- 使用终端进入字体存放目录，运行 `unzip windowsFonts.zip` 解压字体包（如果下载的是压缩包）。
- 安装字体：运行 `fc-cache -fv` 命令来更新字体缓存，确保系统识别新字体。
- 验证安装：通过 `fc-list | grep '宋体'` 确认宋体已被成功安装。

### 3. 配置Flowable

在Spring Boot项目中，创建或修改配置类，加入以下代码片段：

```java
@Configuration
public class FlowableConfig implements EngineConfigurationConfigurer<SpringProcessEngineConfiguration> {
    @Override
    public void configure(SpringProcessEngineConfiguration engineConfiguration) {
        // 设置活动、标签、注解字体为宋体，以支持中文
        engineConfiguration.setActivityFontName("宋体");
        engineConfiguration.setLabelFontName("宋体");
        engineConfiguration.setAnnotationFontName("宋体");
    }
}
```

确保此配置文件生效且无误。

### 4. 流程图生成代码示例

在生成流程图的控制器中，确保调用`generateDiagram`方法时使用了正确的字体名称：

```java
// 示例代码省略部分导入语句
BpmnModel bpmnModel = repositoryService.getBpmnModel(pi.getProcessDefinitionId());
ProcessEngineConfiguration engconf = processEngine.getProcessEngineConfiguration();
ProcessDiagramGenerator diagramGenerator = engconf.getProcessDiagramGenerator();
InputStream in = diagramGenerator.generateDiagram(
    bpmnModel, "png", activityIds, flows,
    engconf.getActivityFontName(), engconf.getLabelFontName(),
    engconf.getAnnotationFontName(), engconf.getClassLoader(), 1.0, false);
// ……剩余的流出流处理逻辑
```

### 5. 测试与验证

完成上述步骤后，重新启动应用服务。通过应用访问流程图界面，检查中文是否已正常显示，无乱码现象。

---

以上步骤将指导您顺利完成Flowable工作流部署到服务器后，解决生成流程图中文乱码的问题。记得每次修改配置后都需要测试验证效果，确保最佳用户体验。

## 下载链接

[Flowable工作流部署解决中文乱码教程](https://pan.quark.cn/s/b91a5e8bf5a6)