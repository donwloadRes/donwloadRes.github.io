---
layout: post
title: "Android TextView 字体设置指南
date   20231102
tags 字体Android设置TextViewttf
comments true
author admin

 Android TextView 字体设置指南

本资源文件提供了关于如何在 Android 应用中为 TextView 设置第三方字体全局字体以及在 Android X 环境下进行字体设置的详细指南通过本指南开发者可以轻松实现自定义字体提升应用的用户体验

 内容概述

1 第三方字体设置
    如何在 Android 应用中引入并使用第三方字体文件如 ttf 格式
    通过代码动态设置 TextView 的字体

2 APP 全局字体设置
    如何在应用中全局设置自定义字体使所有 TextView 默认使用该字体
    使用 Calligraphy 库简化全局字体设置过程

3 Android X 字体设置
    在 Android X 环境下如何处理字体设置避免兼容性问题
    使用 ViewPump 库解决 Android Q 及 Android X 环境下的字体设置问题

 使用方法

 1 第三方字体设置

将字体文件如 ttf放置在 assets 目录下然后通过以下代码设置 TextView 的字体

java
Typeface typeface  TypefacecreateFromAssetgetAssets fontsyourfontttf
textViewsetTypefacetypeface


 2 APP 全局字体设置

1 引入 Calligraphy 库
   gradle
   implementation ukcochrisjenxcalligraphy220
   

2 在 Application 类中初始化 Calligraphy
   java
   public class MyApplication extends Application 
       Override
       public void onCreate 
           superonCreate
           CalligraphyConfiginitDefaultnew CalligraphyConfigBuilder
               setDefaultFontPathfontsyourfontttf
               setFontAttrIdRattrfontPath
               build
       
   
   

3 在 AndroidManifestxml 中配置自定义 Application
   xml
   application
       androidnameMyApplication"
date:   2023-11-02
tags: [字体,Android,设置,TextView,ttf]
comments: true
author: admin
---
# Android TextView 字体设置指南

本资源文件提供了关于如何在 Android 应用中为 TextView 设置第三方字体、全局字体以及在 Android X 环境下进行字体设置的详细指南。通过本指南，开发者可以轻松实现自定义字体，提升应用的用户体验。

## 内容概述

1. **第三方字体设置**
   - 如何在 Android 应用中引入并使用第三方字体文件（如 `.ttf` 格式）。
   - 通过代码动态设置 TextView 的字体。

2. **APP 全局字体设置**
   - 如何在应用中全局设置自定义字体，使所有 TextView 默认使用该字体。
   - 使用 Calligraphy 库简化全局字体设置过程。

3. **Android X 字体设置**
   - 在 Android X 环境下如何处理字体设置，避免兼容性问题。
   - 使用 ViewPump 库解决 Android Q 及 Android X 环境下的字体设置问题。

## 使用方法

### 1. 第三方字体设置

将字体文件（如 `.ttf`）放置在 `assets` 目录下，然后通过以下代码设置 TextView 的字体：

```java
Typeface typeface = Typeface.createFromAsset(getAssets(), "fonts/your_font.ttf");
textView.setTypeface(typeface);
```

### 2. APP 全局字体设置

1. 引入 Calligraphy 库：
   ```gradle
   implementation 'uk.co.chrisjenx:calligraphy:2.2.0'
   ```

2. 在 Application 类中初始化 Calligraphy：
   ```java
   public class MyApplication extends Application {
       @Override
       public void onCreate() {
           super.onCreate();
           CalligraphyConfig.initDefault(new CalligraphyConfig.Builder()
               .setDefaultFontPath("fonts/your_font.ttf")
               .setFontAttrId(R.attr.fontPath)
               .build());
       }
   }
   ```

3. 在 `AndroidManifest.xml` 中配置自定义 Application：
   ```xml
   <application
       android:name=".MyApplication"
       ... >
   </application>
   ```

### 3. Android X 字体设置

1. 引入 ViewPump 库：
   ```gradle
   implementation 'io.github.inflationx:calligraphy3:3.1.1'
   implementation 'io.github.inflationx:viewpump:2.0.3'
   ```

2. 在 Application 类中初始化 ViewPump：
   ```java
   public class MyApplication extends Application {
       @Override
       public void onCreate() {
           super.onCreate();
           ViewPump.init(ViewPump.builder()
               .addInterceptor(new CalligraphyInterceptor(
                   new CalligraphyConfig.Builder()
                       .setDefaultFontPath("fonts/your_font.ttf")
                       .setFontAttrId(R.attr.fontPath)
                       .build()))
               .build());
       }
   }
   ```

3. 在 Activity 中重写 `attachBaseContext` 方法：
   ```java
   @Override
   protected void attachBaseContext(Context newBase) {
       super.attachBaseContext(ViewPumpContextWrapper.wrap(newBase));
   }
   ```

## 注意事项

- 确保字体文件路径正确，避免因路径错误导致字体无法加载。
- 在使用第三方库时，注意版本兼容性，避免因版本问题导致应用崩溃。

通过本指南，您可以轻松实现 Android 应用中的自定义字体设置，提升应用的用户体验。

## 下载链接

[AndroidTextView字体设置指南](https://pan.quark.cn/s/24a6e302b329)