# Android-ADB-Fastboot
[ADB and Fastboot file sources](https://github.com/rendiix/termux-adb-fastboot.git)
> 本库仅供学习交流，如有问题请向源仓库提issues

# CPU支持
arm64-v8a
armeabi-v7a
x86
x86_64

<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/5.jpg" >

# ADB版本
Android Debug Bridge version 1.0.41
Version 33.0.3-vanzdobz@gmail.com
# Fastboot版本
fastboot version 33.0.3

## 特别感谢
感谢rendiix大佬的编译
ʕ ̳• · • ̳ʔ
/ づ♡ =͟͟͞͞♡
## 无Root安装教程
### 在Termux内运行
[点这下载Termux](https://wwu.lanzoul.com/iB8ZD03r51eb)
密码：dsfb

### 下载ADB工具
```
apt install wget && apt install zip && cd && rm -rf ADB-termux.zip && wget https://raw.githubusercontent.com/liyw0205/Android-ADB-Fastboot/main/ADB-termux.zip && unzip -oq "ADB-termux.zip" && rm -rf ADB-termux.zip && rm -rf ADB && mv 安卓ADB环境 ADB && chmod -R 777 ADB
```
**安卓12专版**
```
apt install wget && apt install zip && cd && rm -rf ADB-termux.zip && wget https://raw.githubusercontent.com/liyw0205/Android-ADB-Fastboot/main/ADB-termux-12.zip && unzip -oq "ADB-termux.zip" && rm -rf ADB-termux-12.zip && rm -rf ADB && mv 安卓ADB环境 ADB && chmod -R 777 ADB
```
### 运行ADB菜单
> 配置环境后可不借助菜单直接运行ADB命令
```
cd && cd ADB && bash 菜单.sh
```
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/1.jpg" >
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/2.jpg" >

## 有Root安装教程
### 在MT管理器内运行
[点这下载MT管理器](https://binmt.lanzouy.com/b01bivkzc)

### 下载ADB工具
```
https://raw.githubusercontent.com/liyw0205/Android-ADB-Fastboot/main/ADB.zip 
```
**安卓12专版**
```
https://raw.githubusercontent.com/liyw0205/Android-ADB-Fastboot/main/ADB.zip 
```
### 运行ADB菜单
> 打开MT管理器
>> 配置环境后输入以下命令可不借助菜单直接运行ADB命令
>>> 
```
cp -af /data/wowull/ADB/adb /system/bin/ && cp -af /data/wowull/ADB/fastboot /system/bin/
```
解压ADB工具
以root权限执行菜单.sh
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/3.jpg" >
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/4.jpg" >

# OTA连接教程
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/6.jpg" >

> 先配置ADB环境
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/11.jpg" >

> 手机A：开启**开发者模式**，开启**USB调试**，打开**OTG**
>> 手机**B**开启同手机**A**
>>> 然后手机**A当**主机 手机**B**当副机

OTG转接口插**A**
数据线插**B**
或者双头Type-c/micro数据线（先插**A**后插**B**）
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/7.jpg" >

开启循环申请USB调试，如果手机B不弹USB调试则拔插B那头的数据线直至获得USB调试
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/8.jpg" >

手机B：√上一律允许使用这台计算机调试，然后再点允许
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/9.jpg" >

手机B：√上一律允许使用这台计算机调试，然后再点允许
<img src = "https://github.com/liyw0205/Android-ADB-Fastboot/raw/main/10.jpg" >

# 目前已知问题
fastboot reboot-recovery（fb重启至rec）仅一些设备可以成功重启至rec，其它则重启了设备