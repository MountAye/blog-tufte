---
layout:  post
title:  ".sh | 在 VirutalBox 中安装 Arch Linux"
keywords: md
excerpt: "这是一篇速记，相当于实验的原始记录。日后有可能根据这些记录，整理出一些心得体会，或者全流程的教程。"
date:    2019-09-03
categories: post
milestoneID: 9
---

> 这是一篇速记，相当于实验的原始记录。日后有可能根据这些记录，整理出一些心得体会，或者全流程的教程。

第四代树莓派（[Raspberry Pi 4](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/)）刚刚推出的时候，脑子一热买了一台。作为一台计算机，只用原装的操作系统有点咸鱼了，所以打算安装 Linux 的一款发行版。既然要追求刺激，那就贯彻到底咯，于是就决定挑战一下 Arch Linux。 ~~（反正早晚也要吃灰）~~

既然要挑战一个很有挑战性的操作系统，那么先在虚拟机里试试水就很有必要了。（后来才发现用这个虚拟机往树莓派里写操作系统，也是官方比较推荐的一种安装方式。）于是就开始了这篇速记中的一系列折腾。

## 我的硬件和软件配置

* **硬件**：蓝厂 CPU、绿厂显卡、2*8 GiB 内存、小 SSD + 大 HDD 硬盘、iTX 主板，机龄不到两年，日常可以流畅使用。
* **物理机操作系统**：Windows 10 Pro
* **虚拟机控制软件**：VirtualBox 6.10，短暂用过 5.12 版本
* **虚拟机镜像文件**：Arch Linux 2019.08.01, Windows 10, Fedora 30 Workstation

## 虚拟机托管软件 VirtualBox

可以看一下编程随想的博客里的 [系列文章](https://program-think.blogspot.com/2012/10/system-vm-0.html)。

我的手头一直有虚拟机托管软件，但是没有编程随想那样的需求，平时几乎用不到。（用虚拟机学 Linux？你可拉倒吧）不过之前很轻松地装过一些 Linux 的发行版，主要是 Fedora，所以没觉得这部分会有什么问题，直接开始了主线任务：下载 Arch Linux 的安装 ISO 镜像、检查校验和（FCIV，教程可以看 [这里](https://program-think.blogspot.com/2013/02/file-integrity-check.html)）、按照官网 [安装指南](https://wiki.archlinux.org/index.php/Installation_guide)（[中文](https://wiki.archlinux.org/index.php/Installation_guide_(%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87))）操作，然后发现虚拟机连不上网 :-(

### 问题：虚拟机无法通过 NAT 或 NAT Network 模式联网

具体表现为 `ping www.google.com` 报错：

``` bash
> ping archlinux.org
# Temporary failure in name resolution
```

此时的网络设置没有修改过，就是几乎没有可选参数的 NAT 模式。

第一反应当然是把报错的信息直接复制粘贴到 Google 里，然后看到了 [这个帖子](https://bbs.archlinux.org/viewtopic.php?id=237461)。

回答用一种很有礼貌的方式表述了 RTFM，并给出了官方的 [Network Configuration 页面](https://wiki.archlinux.org/index.php/Network_configuration)。

按照这个页面的步骤，因为我的 ISP 给的是动态的 IP，需要用DHCP，DHCP 是啥我都不知道，搞得我跪着下载了编程随想书单里的《Richard Stevens TCP-IP 详解》，解压后看着 3 卷一百多个 PDF 文件，默默关上了资源管理器……

继续变换关键词搜索解决方案，在这期间改动过防火墙设置，又重置了一次；重装了两次旧版本 VirtualBox，因为第一次重装忘记删除配置信息（Windows 10 Pro 在 `%userprofile%\.virtualbox`，见[这个帖子](https://superuser.com/a/1429931)）；另外装了 Windows 10 和 Fedora 30 两个虚拟机；找来一个玩过 VirtualBox 而且打包票能解决问题的同学。确定了和虚拟机中的操作系统无关，VirtualBox 的 Bridge 桥接模式是可以联网的，但是总不能放任虚拟机的重要联网功能残废着啊 ~~（何况 NAT 模式在多重代理中不可或缺）~~，还是一筹莫展。

就在折腾了这么几天之后，Windows 推送了一次更新，神奇的一幕发生了！更新之后，不论是 NAT 还是 NAT Network 模式，虚拟机都能正常上网，所以，可能真的是“天下本无事，庸人自扰之”吧……

**解决方法：~~吃饭睡觉打豆豆~~**

## 安装 Arch Linux

继续按照官方指南进行安装，不得不说这份指南写的真的不好，至少对于新手是不友好的。一个典型的例子就是下面这句：

> 你需要安装 Linux 引导程序以在安装后启动系统，你可以使用的的引导程序在 [启动加载器]() 中，请选择一个并且安装并配置它，比如 [GRUB]()。

你该怎么办？公布一下正确答案：点击 `GRUB` 那个链接，在一众分类中找到适用于你的计算机配置的那一节，目力忽略各种介绍，找到那一两行有用的命令。ε=( o｀ω′)ノ

反正单看这一句，以我的理解能力，我是没办法正常通关，于是就有了下面硬盘格式化的问题。

### 问题：硬盘格式化不正确

我是用 fdisk 进行的硬盘分区，在正常模式之下似乎找不到选择分区类型的选项，所以我的 EFI 分区也被当作了 Linux 文件系统，所以在很多个步骤之后报错，具体的报错信息已经不记得了。

还好在编程随想的博客的评论区里见到过萌狼，一个 Arch Linux 用户，顺手去他家的博客逛了逛，知道他写过一系列关于 Arch 的博客。所以找到了《给 GNU/Linux 萌新的 Arch Linux 安装指南》，于是直接重建了一个空白虚拟机，按照新教程的流程走了一遍。

**解决方法：看[萌狼的安装教程](https://blog.yoitsu.moe/arch-linux/installing_arch_linux_for_complete_newbies.html)，用 cgdisk 分区**

### 问题：开机后显示 UEFI interactive shell

本以为万事大吉，结果卸载掉安装 ISO 之后开机，总是会进入 UEFI interactive shell。输入 `exit` 之后重新开始倒计时，然后再次进入这个 shell……

就在写这篇速记的时候，我找到了官方 wiki 的 [这个条目](https://wiki.archlinux.org/index.php/GRUB_(%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87)#%E5%90%AF%E5%8A%A8%E6%97%B6%E8%BF%9B%E5%85%A5%E4%BA%86%E6%95%91%E6%80%A5%E6%8E%A7%E5%88%B6%E5%8F%B0)，理论上应该是针对这个问题的，但是看一下就知道，并没有提供可操作的解决方案。

通过 STFW，找到了这篇文章：《[如何在 VirtualBox 内安装 Arch Linux](https://cli.ee/archlinux-virtualbox)》，里面提到这个问题是由 VirtualBox 的 UEFI 引起的，同时提供了解决方法：

```bash

Shell> bcfg boot dump -v              # 查看启动的菜单
Shell> bcfg boot rm 0                 # 删除光驱启动目录
Shell> fs0:                           # 进入 EFI 分区
FS0:\> ls                             # 查看目录，可以看到 EFI 目录
FS0:\> mkdir EFI\boot                 # 在 EFI 目录下创建子目录
FS0:\> ls EFI                         # 查看 EFI 目录，确认是否已创建子目录 boot
FS0:\> cp EFI\grub\grubx64.efi EFI\boot\bootx64.efi # 复制 efi 文件并重命名
FS0:\> exit                           # 退出
```

执行完这一步，开机之后就可以看到 GRUB 的选择操作系统的界面了，因为只安装了 Arch Linux，我们只能看到两个选项，一个 `Arch Linux` 正常启动，一个 `Advanced Options for Arch Linux`。

### 问题：开机后无法进入图形界面

本以为万事大吉，结果开机之后选择 `*Arch Linux` 选项，屏幕上只剩下两行字，然后没有其他反应。

同样是上网搜了一下，发现如果按下 `Ctrl + Atl + F2` 是可以进入命令行模式的，随便执行了几个命令，发现系统工作正常。用 `journalctl` 看一下系统日志，发现在最后一段里经常出现高亮的几行里面，都有 `drm` 这个关键词，再次搜索，发现是和显卡相关的。因为是在虚拟机里，所以就去 VirtualBox 里康康有啥可能会导致问题的选项。

**解决方法：在 VirtualBox 的虚拟机显示设置界面，禁用3D加速**

<hr class="slender">

至此，所有的坑都已经踩完了，开机之后可以看到正常的登录界面，Duang~Duang~~~

{% maincolumn "assets/photos/arch.png" "" %}