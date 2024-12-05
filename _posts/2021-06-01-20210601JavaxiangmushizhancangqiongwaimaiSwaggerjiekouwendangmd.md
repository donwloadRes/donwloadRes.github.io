---
layout: post
title: "Java项目实战苍穹外卖 Swagger接口文档"
date:   2021-03-21
tags: [文档,外卖,Swagger,接口,sky]
comments: true
author: admin
---
# Java项目实战《苍穹外卖》 Swagger接口文档

## 项目简介
《苍穹外卖》是一个Java实战项目，旨在通过模拟外卖服务平台的全栈开发流程，帮助Java开发者提升实际项目开发能力。本项目涵盖了从前端到后端的全套开发流程，并深入探讨了Java在实际应用场景中的强大功能。

## Swagger接口文档
Swagger是一个用于生成、描述、调用和可视化RESTful Web服务的框架。通过Swagger，开发者可以自动生成在线接口文档，减轻后端开发人员的文档编写负担。此外，Swagger与Spring框架高度兼容，通过引入Springfox组件，开发者可以轻松集成Swagger。

### 使用步骤
1. **导入 knife4j 的 Maven 坐标**
   在 `sky-server/pom.xml` 文件中添加以下依赖：
   ```xml
   <dependency>
       <groupId>com.github.xiaoymin</groupId>
       <artifactId>knife4j-spring-boot-starter</artifactId>
   </dependency>
   ```

2. **配置 knife4j 相关配置**
   编辑 `sky-server/src/main/java/com/sky/config/WebMvcConfiguration.java` 文件，添加以下配置：
   ```java
   @Bean
   public Docket docket() {
       ApiInfo apiInfo = new ApiInfoBuilder()
           .title("苍穹外卖项目接口文档")
           .version("2.0")
           .description("苍穹外卖项目接口文档")
           .build();
       Docket docket = new Docket(DocumentationType.SWAGGER_2)
           .apiInfo(apiInfo)
           .select()
           .apis(RequestHandlerSelectors.basePackage("com.sky.controller"))
           .paths(PathSelectors.any())
           .build();
       return docket;
   }
   ```

3. **设置静态资源映射**
   编辑 `sky-server/src/main/java/com/sky/config/WebMvcConfiguration.java` 文件，添加以下配置：
   ```java
   protected void addResourceHandlers(ResourceHandlerRegistry registry) {
       registry.addResourceHandler("/doc.html")
           .addResourceLocations("classpath:/META-INF/resources/");
       registry.addResourceHandler("/webjars/**")
           .addResourceLocations("classpath:/META-INF/resources/webjars/");
   }
   ```

4. **访问文档**
   接口文档地址：`http://localhost:8080/doc.html`

### 常用注解
通过注解可以控制生成的接口文档，使接口文档拥有更好的可读性。常用注解如下：
- `@Api`：用在类上，例如Controller，表示对类的说明。
- `@ApiModel`：用在类上，例如entity、DTO、VO。
- `@ApiModelProperty`：用在属性上，描述属性信息。
- `@ApiOperation`：用在方法上，例如Controller的方法，说明方法的用途、作用。

## 项目资源
本仓库提供了《苍穹外卖》项目的Swagger接口文档资源文件，供开发者参考和使用。

## 联系我们
如有任何问题或需要进一步的帮助，请联系我们。

## 下载链接

[Java项目实战苍穹外卖Swagger接口文档](https://pan.quark.cn/s/938c874a7963)