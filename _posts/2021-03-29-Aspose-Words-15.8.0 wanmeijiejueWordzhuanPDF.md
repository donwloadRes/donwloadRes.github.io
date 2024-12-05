---
layout: post
title: "Aspose-Words-15.8.0 完美解决Word转PDF"
date:   2022-10-29
tags: [PDF,Word,15.8,Aspose,Words]
comments: true
author: admin
---
# Aspose-Words-15.8.0 完美解决Word转PDF

## 简介

本资源文件提供了Aspose-Words-15.8.0版本的Java库，专门用于将Microsoft Word文档转换为PDF格式。该库功能强大，支持多种操作，能够完美解决Word转PDF的需求，且转换后的PDF文件无水印。

## 功能特点

- **完美转换**：支持将Word文档无缝转换为PDF格式，转换后的PDF文件质量高，无水印。
- **简单集成**：通过简单的配置和代码集成，即可在Java项目中使用该库。
- **支持多种操作**：除了Word转PDF，还支持其他多种文档操作，如文档创建、编辑等。

## 使用方法

### 1. 集成Aspose-Words

首先，您需要下载Aspose-Words-15.8.0的jar包，并将其集成到您的Java项目中。如果您使用的是Maven项目，可以按照以下步骤进行配置：

1. 在项目根目录中创建一个`lib`文件夹，并将jar包放入其中。
2. 在`pom.xml`文件中添加以下依赖配置：

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-words</artifactId>
    <version>15.8.0</version>
    <scope>system</scope>
    <systemPath>${project.basedir}/lib/aspose-words-15.8.0-jdk16.jar</systemPath>
</dependency>
```

### 2. 配置License

为了去除转换后的PDF文件中的水印，您需要配置License文件。将License文件放置在项目的`resources`目录下，并确保其路径正确。

### 3. Word转PDF

以下是一个简单的示例代码，展示如何使用Aspose-Words将Word文档转换为PDF：

```java
public class AsposeUtil {
    /**
     * 加载license 用于破解 不生成水印
     */
    @SneakyThrows
    private static void getLicense() {
        try (InputStream is = AsposeUtil.class.getClassLoader().getResourceAsStream("License.xml")) {
            License license = new License();
            license.setLicense(is);
        }
    }

    /**
     * word转pdf
     * @param wordPath word文件保存的路径
     * @param pdfPath 转换后pdf文件保存的路径
     */
    @SneakyThrows
    public static void wordToPdf(String wordPath, String pdfPath) {
        getLicense();
        File file = new File(pdfPath);
        try (FileOutputStream os = new FileOutputStream(file)) {
            Document doc = new Document(wordPath);
            doc.save(os, SaveFormat.PDF);
        }
    }
}
```

### 4. 打包注意事项

在使用`<scope>system</scope>`引入依赖时，打包时需要注意添加以下配置，以确保Spring Boot能够正确打包本地jar：

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
            <configuration>
                <includeSystemScope>true</includeSystemScope>
            </configuration>
        </plugin>
    </plugins>
</build>
```

## 结语

Aspose-Words-15.8.0是一个功能强大的Word文档处理库，能够完美解决Word转PDF的需求。通过简单的集成和配置，您可以在Java项目中轻松使用该库，实现高质量的文档转换。

## 下载链接

[Aspose-Words-15.8.0完美解决Word转PDF分享](https://pan.quark.cn/s/d8270b00b26e)