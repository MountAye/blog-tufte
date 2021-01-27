---
layout:      post
title:      ".md | 扫盲Barrier，用笔记本键鼠无线控制台式机"
keywords:   md
excerpt:    "你看我这个标题它像不像编程随想:-p"
date:        2020-12-22
categories:  post
milestoneID: 22
---

## 为啥要用 `Barrier`

圣诞节前的周五，我们系在线上办了一个聚会。和学姐闲聊的时候，听说他们高年级的几个朋友每周一起联机玩《文明6》，于是一番理(卑)直(躬)气(屈)壮(膝)的要(恳)求之后，成功加入了组织，等到了 steam 的圣诞特惠（没错我一直没买 new frontier pass，我是云玩家），准备以物理学工作者的严谨态度，研究《文明6》诱导的基于回合的反常时间平移对称现象。

{% maincolumn "assets/photos/2020-12-22-livingroom.png" "" %}

我现在公寓房间的结构如图所示，前任房客走的急，把她的几乎全部家具低价甩卖给我了，四舍五入相当于白捡了一台大电视。电视用 HDMI 线连接电脑，当作第二显示器使用。躺在沙发上，看着大屏幕，玩着文明6，[运用自如](https://www.bilibili.com/video/BV1g441187zq)的话说——“那岂不是非！常！爽！”

所以说，我的要求是：

- 在笔记本和台式机处于同一 Wifi 的情况下——
- 笔记本电脑和台式机之间不需要任何数据线连接
- 使用 Linux 笔记本上的触控板、鼠标和键盘
- 控制 Windows 台式机
- 正常运行和操作《文明6》，不会因为延迟卡顿被人喷（卡顿是不存在的，只可能掉线lol）

一番搜索之后，锁定了 `Barrier` 这款软件。它可以设定一个 server 和多个 client，用 server 的输入设备控制各个 client。切换方法也很方便，只要提前约定好各个设备的“相对位置”，当 server 的鼠标光标跨过 server 屏幕的边角处，就开始控制对应方向上的设备。（具体可以查看下一节。）

之所以选择它，主要原因如下：

- [开源软件](https://github.com/debauchee/barrier)，堂堂正正地不用花钱。（我知道开源软件≠免费软件，但是……）
- 目前依然有人维护，GutHub 上还有上百个 open issues，当然 closed issues 更多，有问题可以查，提问也有人回答。
- 跨平台，Windows 和 Linux 都能用。主流 Linux 发行版都可以在仓库里找到，也可以通过 snap 安装。

## 如何配置 `Barrier`

### 下载和安装：

因为我的发行版是 Fedora，在笔记本的 terminal 上任选一句运行：

```shell

sudo dnf install barrier
sudo snap install barrier
```

台式机是 Windows 10，在GitHub 项目（[链接在此](https://github.com/debauchee/barrier/releases)）里找到最新一期的发布版本，找到 `.exe` 结尾的文件（可以用浏览器的页内搜索），下载，双击下载后的文件安装。

### 配置 server （笔记本电脑）：

首先要确定 linux 的桌面环境是基于 xorg 的，当前版本的 GNOME 默认使用的是 Wayland，所以需要 log out 之后重新选择带有 xorg 字样的环境，如下图：

{% maincolumn "assets/photos/2020-12-22-gnome-environments-new.png" "" %}

安装完成之后，在 app 界面（`Win`+`A`）应该可以找到 barrier 的图标，单击即运行。一般来说之后会有相当长一段时间电脑没有反应，这个时候 **千万不要重复点击图标**，会导致无法连接。

{% maincolumn "assets/photos/2020-12-22-barrier_linux_desktop.png" "" %}

之后会看到软件的主界面，选中图中所示的选项：

{% maincolumn "assets/photos/2020-12-22-barrier_linux_start.png" "" %}

然后单击 `configure server` 按钮，进入下图的界面，拖动右上角的电脑屏幕图标，拖到中间屏幕周围的任意一格。我选了右边一格，因为这样在笔记本上向右滑鼠标会进入台式机的显示器，从显示器右边框向右会进入电视，一路反过来就回到了笔记本屏幕，操作比较自然。

{% maincolumn "assets/photos/2020-12-22-barrier_linux_config.png" "" %}

双击图标后会弹出一个新窗口，在最上面的 "screen name" 栏填入 client 上显示的本机名称，现在我们还没有配置 client，所以需要等到配置完之后回来填写。

{% maincolumn "assets/photos/2020-12-22-barrier_linux_naming.png" "" %}

注意主窗口的左下角，如果不是 “barrier is running” 的话，需要点击右下方的 reload，还是不行的话就要准备 debug 了。

### 配置 client （台式机）：

安装完成之后，应该能在开始菜单里找到 barrier 的图标，点击运行，应该会看到和笔记本上面差不多的界面。

{% maincolumn "assets/photos/2020-12-22-barrier_windows_main.png" "" %}

选择图中的选项，填入笔记本窗口中显示的本机 IP 地址，选中 `auto config` 选项，然后点击右下方的 `start`，然后窗口左下角同样应该有 "barrier is running" 字样。点击菜单栏里的  -> `show log` 打开日志，应该可以看到下图里的 "connected to server" 字样。

{% maincolumn "assets/photos/2020-12-22-barrier_windows_log.png" "" %}

### 几个雷点：

- Fedora 的显示管理器默认并不使用 xorg，需要专门切换。
- Linux 上启动较慢，如果不耐烦多点了几次，可能会重复打开多个实例，造成端口被占用，无法使用。
    + 诊断方法：打开 log 界面，会发现 "ERROR: cannot listen for clients: cannot bind address: Address already in use"  字样。
    + 解决方法：杀掉多余的进程，不会杀的话就重启电脑吧。
- server 和各个 client 对是否使用 SSL 的选择必须是一致的。
- 官方没有按步骤来的配置说明，这么多雷点，我居然看到好几篇博客都在夸 barrier 的界面多么通俗易懂，简直了。 

## `Barrier` 之外的其他方案

- `synergy`：成熟的商业软件，好像要花钱。
- `Microsoft Garage Mouse without Borders`：要求所有设备都使用 Windows 系统，不适用于我的笔记本电脑
- `usbip`：来自 farseerfc 大神的[这篇博文](https://farseerfc.me/zhs/usbip-forward-raspberrypi.html)，原文说“设置好的话，就像是一台 PC 多了几个位于树莓派上的 USB 端口，插上树莓派的 USB 设备统统作为 PC 的设备”。
    + 和 `Barrier` 相比，配置的步骤更繁琐；
    + 好像一次只能控制一台设备（不太懂，如果转发给多个设备的话可能会一起执行相同的操作？）；
    + 好像也不适用于非 USB 接口的设备，比如笔记本的原生键盘和触屏笔；
    + 一旦运行起来，server 的鼠标就不再能够控制自己，所以原文使用了几乎注定吃灰的树莓派，相当于给键盘加了个广播天线。

<!-- 用的是一款叫作 [Gather](https://gather.town/) 的 web 应用，就像 90 年代的 RPG 游戏一样，参加者每人指挥一个像素很糊的人物，在一个像素很糊的房间里走来走去，不同之处在于当角色相互靠近到一定距离之内的时候，可以像 Zoom 一样视频连线。 -->