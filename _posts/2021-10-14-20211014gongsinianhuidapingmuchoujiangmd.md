---
layout: post
title: "公司年会大屏幕抽奖"
date:   2022-10-22
tags: [签到,bug,抽奖,摇一摇,优化]
comments: true
author: admin
---
# 公司年会大屏幕抽奖

## 简介

本资源文件提供了一个专为公司年会设计的大屏幕抽奖系统。该系统经过多次更新和优化，旨在提供稳定、高效且功能丰富的抽奖体验。无论是签到、抽奖、红包发放还是其他互动环节，该系统都能满足您的需求。

## 主要功能

- **签到功能**：支持多种签到方式，包括3D签到、普通签到等，签到名单可导出。
- **抽奖功能**：支持多轮抽奖，可内定中奖人员，优化了抽奖箱效果。
- **红包功能**：增加了红包发放功能，提升年会互动性。
- **手机端支持**：增加了手机端的观众中奖信息查看功能，方便观众实时了解中奖情况。
- **用户体验优化**：处理了多个细节方面的bug，优化了用户体验。

## 更新日志

### 2017.9.27
- 处理可能出现的重复签到情况。
- 被禁用的用户在刷新签到列表后不再显示。
- 增加了功能的快捷键。

### 2017.9.25
- 增加了手机端的观众中奖信息查看功能。

### 2017.8.30
- 处理了一个开幕墙、闭幕墙的二维码bug。

### 2017.8.25
- 增加了红包功能。
- 3D签到预设图形增加了网格。
- 对对碰里面增加了昵称显示。
- 修复一个幸运数字的bug。

### 2017.9.18
- 优化了很多用户体验细节。
- 处理了一些细节方面的bug。

### 2017.8.25
- 增加了红包功能。
- 3D签到预设图形增加了网格。
- 对对碰里面增加了昵称显示。
- 修复一个幸运数字的bug。

### 2017.8.23
- 增强了一个php配置的兼容性。
- 新手指南优化。
- 砸金蛋中奖人数较多时滚动条无法滚动的问题。
- 摇一摇增加了气球风格。
- 调整后台的一些文字描述。
- 新增中奖列表导出。
- 新手指南更新到8月22日。

### 2017.8.11
- 修复一个循环播放时随机出现重复消息的问题。
- 每场活动现在有独特的活动签到连接，不会出现串场的问题了。

### 2017.8.8
- 可以修改管理员密码。
- 增加开幕墙。
- 增加闭幕墙。
- 大屏幕右上角二维码增加中等大小的显示（3种大小状态，适合各种场景使用）。

### 2017.8.6
- 优化了一些js文件。
- 优化前台登录跳转页面的更新。
- 上墙消息增加了显示方式、循环播放设置、循环信息条数、放大显示图片消息开关、放大显示图片消息时间设置。
- 后台关闭上墙、摇一摇、投票后，手机端的菜单也会相应的消失，并且如果不小心连接放错了，可以跳转到签到页面去。
- 系统会自动生成二维码。
- 安装好之后有更多的默认设置可以用，减少配置，即装即用。

### 2017.8.5
- 可以后台修改2段欢迎文字。
- 新手指南更新。
- 修复一个投票页面全屏后背景消失的问题。
- 增加了上墙首页右下角logo的上传功能。
- 相册更新。
- 处理一个在部分服务器上上传会报错的bug。
- 修复一个影响部分服务器的session相关的系统错误。
- 新增文字弹幕。
- 解决了砸金蛋每次只能砸1个人的问题。
- 优化了抽奖箱的效果，声音和摇晃的动作更加符合现实。

### 2017.8.2
- 优化签到顺序号码，减少不连续的情况出现。
- 增加最新的新手使用指南。
- 修复一个使用自己公众号授权的时候页面不跳转的问题。
- 现在可以自己编辑3D签到的图形的顺序及数量。
- 3D签到增加支持文字。
- 3D签到增加倒计时支持。
- 3D签到增加3个控制参数。

### 2017.7.27
- 新增内定列表，方便查看和管理内定人员信息。

### 2017.7.26
- 屏蔽用户的效果能正常运行了。
- 给抽奖箱和砸金蛋增加抽奖内定功能。
- 修复一个摇一摇后台显示错误的bug。
- 新版后台增加了开启和关闭签到填写姓名和手机号功能。

### 2017.7.24
- 优化界面。
- 优化手机页面的跳转。
- 增加签到名单导出功能。

### 2017.7.6
- 对对碰更新。
- 去掉后台进入摇一摇的链接（已经不需要了）。
- 一个可能会跳转到404页面的错误。
- 新版摇一摇菜单不正常显示的问题。
- 抽奖重新抽奖清空数据报错的问题。
- 优化了3D签到的效果。

### 2017.7.5
- 新增幸运手机号。
- 新增砸金蛋。
- 修复一个签到头像可能会重复出现的问题。
- 功能菜单修改。

### 2017.7.4
- 新增幸运号码抽奖。

### 2017.7.3
- 版本号从今天开始改为类似201707021这种形式，前八位是大版本日期，后面的数字是小版本的序号。

### 2017.7.2
- 前端UI界面全部优化。
- 抽奖支持多轮抽奖，可以内定。

### 2017.6.25
- 摇一摇功能全面优化升级，支持多轮摇一摇游戏。

### 2017.6.14
- 现在对对碰签到完成即可参与。
- 优化手机签到页背景。
- 部分文字说明更新。
- 优化了摇一摇功能。
- 图片上传功能优化，上传速度更快，支持jpg和png。

### 2017.6.7
- 去除不常用的功能，拍拍乐，拔河。
- 简化代码，优化性能。
- 系统不再需要对接公众号，使用更方便更自由。
- 修复了一个在windows系统下session可能失效的bug。
- 去除了公众号对接指南。
- 去除数据库中很多不再使用的表和字段，并且增加了大量备注。
- 重新写了签到功能。

### 2017.6.6
- 3D签到功能优化。

### 2017.5.18
- 更新图片保存的相关功能。
- 简化程序。

### 2017.5.17
- 修改session保存方式。

### 2017.5.16
- 修改缓存类，使代码更简介，结构性更好，方便二次开发。
- 修复摇一摇系统使用memcache的一些bug。

### 2017.5.13
- 简化所有主题的界面。
- 优化了后台系统设置页的内容，去掉了已经不用的项目。

### 2017.5.10
- 优化了3D签到的效果，减少屏幕分辨率对效果的影响。

### 2017.5.5
- 开场界面更新。
- 视屏背景主题的视频更新。
- 简化默认自定义主题的界面，使用更方便简洁。
- 修复一个拔河的默认没有自动安装上的问题。

### 2017.5.2
- 新增拔河功能。

### 2017.4.24
- 可以自定义修改版权信息。

### 2017.4.13
- 进一步提升摇一摇性能，减少数据库数据库访问次数。
- 改进完善微信上墙使用教程。

### 2017.4.5
- 修复一些小bug。

### 2017.4.1
- 修复了后台的信息显示的一个bug。

### 2017.2.14
- 优化签到列表的数据读取方式，现在几千人的活动，也不会卡在列表处了。

### 2017.2.13
- 增加了后台可以删除已审核信息的功能。

### 2017.2.7
- 优化抽奖功能，记录每个人被抽中的时间。

### 2017.1.25（数据库结构发生变化）
- 投票管理删除投票项功能。
- 可以设置2D签到时显示的微信昵称，真实姓名和手机号。
- 优化了上传图片的功能，增加了默认值，现在安装完成后不需要再上传自定义的图片才能正常显示页面了。
- 新增自定义上传摇一摇背景图。

### 2017.1.24（数据库结构发生变化）
- 新增签到触发关键字，可以设置关键字来触发签到的图文信息。
- 抽奖可以设置显示签到时填写姓名或手机号。
- 优化拍拍乐的参数设置。

### 2017.1.23
- 优化默认值，使系统安装完成之后设置简化。

### 2017.1.22（数据库结构发生变化）
- 修改了对公众号发送帮助后返回的信息内容，稍微简化了摇一摇和投票的流程。
- 把上传的图片存放目录转到更合适的目录下。

### 2017.1.14
- 解决弹幕必须循环播放的问题。

### 2017.1.10
- 修改了拍拍乐的多个bug。
- 修改了拍拍乐的图片排序。
- 修改了多个主题上墙内容重复滚动的问题。

### 2016.12.30
- 修改了新年主题的对联，改到鸡年的对联。

### 2016.12.16
- 处理了参与抽奖的人数大于150人时的一个人数显示错误。

### 2016.11.22
- 文字提醒优化。

### 2016.11.14
- 摇一摇显示人数的bug。

### 2016.9.23
- 处理一个数据库的兼容问题。
- 修改了多个js bug。
- 修改了smarty 的缓存目录，统一都放到data目录下，避免出现没有权限的情况。
- 优化用户信息获取方法，减少接口使用次数，避免现场观众太多导致接口次数用完的问题。
- 优化系统设置界面，让人更容易看懂，为之后新增功能做准备。
- 现在支持所有类型的公众号。

### 2016.9.12
- 处理一个微信墙js失效的bug。

### 2016.9.9
- 摇一摇前台页面新增重置按钮，方便进行第多轮活动。
- 简化数据库，并提供数据获取的性能。
- 调整系统后台细节，更方便使用。

### 2016.9.7
- 优化抽奖功能，千人万人抽奖都不卡。
- 签到名单导出按钮，在php5.3以下的版本中自动不显示。
- 新增图文并茂的微信上墙使用教程word文档。

### 2016.9.5
- 提高摇一摇性能。
- 修复一个显示图片时候点击抽奖、摇一摇、投票界面，会被自动弹出的bug。

### 2016.9.1
- 新增关键字触发自动回复功能。
- 微信上墙成功后自动回复后可增加自定义文字。

### 2016.8.29
- 增加了程序和服务器的兼容性。
- 增加了系统内置的后台帮助信息。
- 新增签到用户列表导出excel。
- 增加更新日志按钮，最新更新一目了然。

### 2016.8.18
- 优化程序，降低误操作可能性。
- 更新拍拍乐，修复了一些小bug。

### 2016.8.18
- 修改了所有主题的3D签到按钮。
- 普通签到功能优化，修复了一个小bug。

### 2016.8.3
- 修改可以设置抽奖条件签到即可抽奖和签到并发消息才可参与抽奖。

### 2016.8.2
- 修复抽奖结果查询bug，现在不是认证的号可以通过查询的方式获得中奖信息，认证的号在抽中的时候可以直接发送消息提醒中奖。

### 2016.7.22
- 3D签到墙修复不会实时更新签到用户的信息的bug。

### 2016.7.21
- 处理一些兼容性问题。

### 2016.7.18
- 修复拍拍乐抽奖阶段头像不显示bug。

### 2016.7.16
- 抽奖内定功能更新，优化设置流程。
- 美化授权成功页面。

### 2016.7.15
- 优化3D签到墙。
- 优化签到流程，使用更方便。

### 2016.7.14
- 新增3D签到墙。

### 2016.7.13
- 增加了后台的memcache配置功能，开始缓存后性能大大提升哦。

### 2016.7.11
- 修复一个宇宙弹幕不显示内容的bug。

### 2016.7.7
- 修复了一个最近更新中出现的sql语句错误。
- 修复可能导致借用公众号无法获取到用户信息的bug。

### 2016.7.2
- 修改了签到方式，签到更简单，更美观，可后台自定义记录姓名和手机号。

### 2016.6.14
- 修复了一个安装失败的bug。

### 2016.6.11
- 未认证订阅号和未认证服务号上墙功能。
- 修改了部分代码，方便阅读。
- 去掉了，很多不再使用的代码和注释，减少系统体积。
- 修改了 安装配置说明.txt。

### 2016.6.6
- 一键安装中增加了拍拍乐安装功能。

### 2016.6.2
- 微信菜单功能现在支持php5.4以下的版本。

### 2016.6.1
- 某些服务器上安装会出现微信token验证失败的一个问题。
- 数据库文件中的一个语法错误。

### 2016.5.28
- 支持本地缓存memcache，大幅提高摇一摇性能。

### 2016.5.27
- 微信菜单管理。
- 增加默认设置，一键触发帮助，摇一摇，拍拍乐，投票。

### 2016.5.17
- 宇宙弹幕主题，可以设置循环播放是否开启。
- 新增拍拍乐。

### 2016.5.14
- 增加了一些代码注释。
- 强化了代码的兼容性。

### 2016.5.7
- 数据获取方式调整，减少网络流量，性能更好。

### 2016.3.30
- 美化摇一摇手机端界面。

### 2016.3.28
- 增加了抽奖内定功能。
- 去除签到页，改成用手机号签到，方便兑奖。
- 认证订阅号也可以使用。

### 2016.3.25
- 优化了摇一摇的操作，摇动记录功能更灵敏。

### 2016.3.18
- 降低了后台配置难度，使配置更简单。
- 增加了必填项的引导填写功能，操作更简单便捷。

### 2016.3.9
- 上墙首页关注部分的效果，提升了用户体验。
- 摇一摇参与界面的部分效果，提升了用户体验。
- 摇一摇背景变更，提升了用户体验。

### 2016.1.30
- 解决后台未审核信息类型错误的bug。
- 微信墙的一些细节更新，用户体验更好。

### 2016.1.29
- 修改系统的部分程序结构和目录结构。
- 修改更新日志结构。

###

## 下载链接

[公司年会大屏幕抽奖](https://pan.quark.cn/s/6e27e39e2bda)