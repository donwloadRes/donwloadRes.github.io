---
layout: post
title: "androidx相关jar资源"
date:   2020-07-29
tags: [jar,AndroidX,androidx,Android,依赖]
comments: true
author: admin
---
# androidx相关jar资源

本仓库提供了必要的AndroidX库文件，旨在帮助开发者轻松迁移至AndroidX，以替代传统的Android Support库。AndroidX是Google推出的一个重大更新，它不仅包含了原有的Support库功能，还对其进行了模块化的改进，便于维护和升级。

## 包含的jar文件

- **androidx.core.jar**：核心库，提供了很多跨组件的功能，如生命周期管理、偏好设置访问增强等。
- **androidx.appcompat.jar**：兼容库，实现了对旧版本Android系统的向后兼容，包括AppCompat Widgets和支持主题。
- **androidx.drawerlayout.jar**：抽屉布局库，用于实现应用侧滑菜单功能，它是Material Design设计规范中的一个重要组成部分。

## 解决的问题

- **无法找到ContextCompat.checkSelfPermission问题**：升级到AndroidX后，原先基于support库的权限检查方法需要调整，这个更新确保了新方法的可用性。
- **替换v4包中的类**：对于仍然依赖于v4支持库中的ActionBarDrawerToggle、DrawerLayout等类的应用，这些jar文件提供直接的替换选项，使代码能够顺利运行在最新的Android环境上，同时保持功能完整性。

## 使用指导

1. **迁移准备**：在开始之前，建议先备份您的项目，确保有恢复点。
2. **启用AndroidX**：在项目的build.gradle文件中，添加以下两行来启用AndroidX：
   ```gradle
   android.useAndroidX=true
   android.enableJetifier=true
   ```
3. **替换依赖**：移除原有support库的依赖，并将对应的依赖改为AndroidX版本。具体依赖名称请参照最新文档或已提供的jar直接引用。
4. **导入jar文件**：将下载的这三个jar文件放入项目的`libs`目录下（如果没有，则需手动创建），然后在build.gradle中添加对应jar的编译指令：
   ```gradle
   dependencies {
       implementation fileTree(dir: 'libs', include: ['*.jar'])
       // 其他依赖...
   }
   ```
5. **解决编译问题**：完成上述步骤后，可能需要处理因迁移引起的编译错误或警告，遵循IDE给出的建议进行修正。
6. **测试应用**：迁移后务必全面测试应用程序，确保所有功能正常工作。

### 注意

- 迁移到AndroidX是一个系统性的过程，可能会遇到各种依赖冲突或代码不兼容的问题，请参考官方文档或社区指南进行解决。
- 随着Android开发环境的不断更新，推荐直接使用Gradle依赖管理方式获取最新库，以获得持续的支持和更新。

通过使用这些AndroidX相关的jar文件，您将能有效简化从旧版Support库向AndroidX的过渡过程，让您的应用更加现代化并兼容未来版本的Android系统。

## 下载链接

[androidx相关jar资源](https://pan.quark.cn/s/5272ab707f4c)