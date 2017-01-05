---
layout: post
title: "安装 Windows ME"
date: 2017-01-05 09:20
comments: true
categories:
---

人上了年纪，就容易怀旧。

前几天整理房子，翻出10年前买的盗版游戏光盘，又想重温一下以前的感觉。

那个年代，没有网络，电脑机能也比较差，游戏靠的就是高质量和优秀的故事情节来吸引人。

但是尝试安装了几个游戏之后，发现大部分游戏都不支持新的系统了。

于是就开始尝试在 VirtualBox 上安装老的系统。在它的官网查到它的显示驱动只支持到 Windows 2000，但是为了体验纯粹的 9x 系统，还是准备安装 Windows ME。

说干就干，第一个问题就是找 Windows ME 的 ISO。这个可以通过百度云搜索来找。

下载了以后，不能光盘启动。于是用 UltraISO 提取了一个可启动光盘的 boot ，然后再写入 Windows ME 的 ISO，可以启动了。

然后开始分区，使用 fdisk，我测试的时候，只准备分 C 盘，所以一路回车，然后程序提示重启。回到光盘启动以后，运行 format c: 格式化

下一步是切换到光盘盘符，运行 setup 就开始安装了

这里需要说一下，在第一轮安装，复制完文件以后，在重启之前，需要将安装盘的 ISO 从虚拟光驱中卸载了，否则重启以后会有问题。

这样重启以后，就等最后安装完毕。

接下来需要安装显卡驱动，由于之前说的 VirtualBox 官方不支持了，只有找第三方的。

从 http://bearwindows.zcm.com.au/vbe9x.htm 下载最新驱动包，然后解压出来，用 UltraISO 打包成 ISO 用 VirtualBox 加载。

最新的通用显卡驱动没有 Uni 的文件夹了，我用的是 032MB 目录下的驱动，这个是对应的 32MB 显存的显卡。在 VirtualBox 里我只分配了 32MB，够用了，我第一个显卡还是 8M 的 Intel i740

Windows 98 安装方式和这个一样，不过安装重启不用卸载 ISO。

最后上一张最后的 Windows ME 的桌面
<img src="{{ site.url }}Emoticons/2017/WindowsME.png" alt="" align="center" />
