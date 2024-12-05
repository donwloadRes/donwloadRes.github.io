---
layout: post
title: "SpringBoot集成Spring Security、OAuth2实现授权码模式"
date:   2020-02-20
tags: [oauth,Redis,授权,项目,认证]
comments: true
author: admin
---
# SpringBoot集成Spring Security、OAuth2实现授权码模式

## 项目描述

`springboot-security-oauth2` 是一个基于SpringBoot的项目，集成了Spring Security和OAuth2，实现了资源访问的授权认证。该项目支持多种认证模式，包括`client credentials`、`password`和`authorization code`。默认情况下，项目采用了最为复杂的`authorization code`授权码认证模式，并实现了自定义的登录页、授权页、错误页，以及第三方用户登录功能。

## 主要功能

1. **支持的OAuth2端点**：
   - `/oauth/authorize`
   - `/oauth/token`
   - `/oauth/refresh_token`
   - `/oauth/error`

2. **Token存储**：
   - 默认使用`RedisTokenStore`将用户认证的`accessToken`保存在Redis中。
   - 代码中已经支持`JDBC`持久化存储Token，但目前处于注释状态。如果需要使用`JDBCTokenStore`，可以使用以下SQL语句创建相应的数据表：
     ```sql
     USE `iot_boss`;
     ```

## 使用说明

1. **克隆项目**：
   ```bash
   git clone https://github.com/yourusername/springboot-security-oauth2.git
   ```

2. **配置Redis**：
   - 确保本地或远程Redis服务正常运行。
   - 在`application.properties`或`application.yml`中配置Redis连接信息。

3. **启动项目**：
   - 使用IDE（如IntelliJ IDEA或Eclipse）导入项目并启动。
   - 或者使用Maven命令启动：
     ```bash
     mvn spring-boot:run
     ```

4. **访问应用**：
   - 打开浏览器访问`http://localhost:8080`，根据提示进行登录和授权操作。

## 注意事项

- 如果需要切换到`JDBCTokenStore`，请取消相关代码的注释，并确保数据库中已创建相应的数据表。
- 项目默认使用`authorization code`模式，如果需要切换到其他认证模式，请修改相关配置。

## 贡献

欢迎提交Issue和Pull Request，共同完善该项目。

## 许可证

该项目采用MIT许可证，详情请参阅`LICENSE`文件。

## 下载链接

[SpringBoot集成SpringSecurityOAuth2实现授权码模式](https://pan.quark.cn/s/3e8570583991)