---
title: Windows 优化与美化
top: false
img: 'https://s3.bmp.ovh/imgs/2022/05/25/5cb6105a6f337fe1.jpg'
tags: 优化与美化
categories: Windows
abbrlink: 2221957461
date: 2022-05-31 18:51:06
password:
keywords:
---

# 前言

Windows 优化美化基于10以上系统

## Windows 优化

### 关闭系统更新（可选）

#### 禁用更新的优缺点

- 优点

  系统资源占用小

  系统网速提升大

  减少突然更新带来的问题

- 缺点

  系统新功能不能使用

  系统漏洞不能及时修复，系统安全性低

#### 软件下载

- [Windows Update Blocker](https://wwc.lanzoum.com/iFxzO0616lrc)

### 关闭系统实时保护（可选）

Win+R 运行以下命令

```复制
gpedit.msc
```

如图所示 计算机配置-----管理模板-----Windows组件----Microsoft Defender 防病毒----双击打开

![](https://s3.bmp.ovh/imgs/2022/06/07/fd530fc941bcc3f3.png)

勾选“已启用”选项，就可以关闭Windows defender

![](https://s3.bmp.ovh/imgs/2022/06/07/8e9457486af816f0.png)

还是这个页面， 找到 **实时保护** 点进去，同样的操作

![](https://s3.bmp.ovh/imgs/2022/06/07/0fd9abceb7c0ed1a.png)

![](https://s3.bmp.ovh/imgs/2022/06/07/3e7b1c28523bc31a.png)

### 关闭用户账户控制（UAC）

#### 为什么要关闭

关闭后打开任何软件和文件不会再弹出 UAC 提示

Win+R 运行下面命令

```复制
msconfig
```

找到工具----更改 UAC 设置----启动----拉到最低----确定

![](https://s3.bmp.ovh/imgs/2022/06/07/e2410f7222a10355.png)

### 关闭 Windows 防火墙

#### 关闭的优缺点

- 优点

  不会出现游戏公屏以及语音频道的互通问题等等

- 缺点

  无法防止计算机病毒和蠕虫进入计算机

  系统不会询问是否允许或阻止某些连接请求

  无法阻止未授权的用户通过互联网对计算机的访问

  无法防止计算机内部信息的泄露

打开控制面板----系统和安全----Windows Defender 防火墙----启动或关闭 Windows Defender----全部关闭

### 关闭系统服务（可选）

Win+R 运行下面命令

```复制
services.msc
```

按照下表根据需要关闭

|            服务名称             |                          说明                           |
| :-----------------------------: | :-----------------------------------------------------: |
|   Bluetooth Handsfree Service   |                 没有蓝牙的用户可以关闭                  |
|           Smart Card            | 管理计算机对智能卡的读取访问，没有安装UPS的用户可以禁用 |
|          Print Spooler          |                没装打印机可以禁止该服务                 |
|         Security Center         |                   Windows安全中心服务                   |
|               Fax               |                 传真资源发送和接收传真                  |
|         Windows Backup          |                 Windows 备份和还原功能                  |
| Windows Error Reporting Service |                      错误报告传送                       |
|         Windows Update          |                      系统自动更新                       |
|        Windows Firewall         |                     Windows 防火墙                      |

## Windows 美化

### 猫猫回收站

打开桌面图标设置

![](https://s3.bmp.ovh/imgs/2022/06/07/329b7b6b3be1e2b4.png)

选择回收站更换图标

![](https://s3.bmp.ovh/imgs/2022/06/07/2fea0955c59e550f.png)

####  图标下载

- [下载链接](https://wwc.lanzoum.com/iXftB05p0jaf)
