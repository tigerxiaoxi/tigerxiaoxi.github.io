---
layout:     post
title:      用36张图片教你使用VMware安装macOS
subtitle:   用36张图片教你使用VMware安装macOS
date:       2025-6-19
author:     Venti__0616
header-img: img/StarTrails.jpg
catalog: false
tags:
    - macOS
---


## 一、准备

需要：
- 虚拟机软件：VMware Workstation Pro
- VMware macOS解锁程序：Unlocker
- macOS系统镜像文件

接下来就开始下载需要的文件。

### （一）安装VMware Workstation Pro

[VMware Workstation Pro 下载链接（提取码cv2A）](https://caiyun.139.com/m/i?1A5Cvaun8nrql)

下载好后解压，双击安装程序，一直点击下一步，直到填写许可证的界面，点击许可证，许可证默认是填好的，点击输入，再点击完成就安装成功了（请注意，不要使用高版本的VMware）。

![](https://cdn.luogu.com.cn/upload/image_hosting/ik627fym.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/kta3uup7.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/9sjq5g4v.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/iwuj4tn5.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/u7sp0kp9.png)

### （二）下载Unlocker

如果VMware在没有使用Unlocker解锁的情况下打开，在选择虚拟机操作系统时就没有Apple Mac OS X的选项，所以我们需要下载Unlocker。

[Unlocker官网](https://github.com/DrDonk/unlocker/releases)

在官网界面，默认显示的是最新版本，下面有一个Assets，点击unlocker<版本号>.zip下载后解压。

![](https://cdn.luogu.com.cn/upload/image_hosting/5it2pnol.png)

工具使用之前要先关掉VMware，后台的VMware进程也要清理干净。右键开始图标，在弹出的窗口选择“任务管理器”，然后往下滑，找到名字带有VMware的进程，全部都右键结束进程。等一会儿，如果有重新弹出来的，也结束掉它们，直到没有一个VMware进程为止。

![](https://cdn.luogu.com.cn/upload/image_hosting/0ke0rddu.png)

然后打开解压好的unlocker<版本号>文件夹，再打开windows文件夹，找到里面叫unlock.exe的程序，右键使用管理员身份运行，运行完之后关闭窗口就可以了。

![](https://cdn.luogu.com.cn/upload/image_hosting/g65oe5lm.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/0bpx4se8.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/xvkawupu.png)

### （三）下载macOS系统镜像文件

接下来是macOS系统镜像文件。两个镜像都可以进行安装。

[macOS Catalina 10.15.7 iso 下载链接（提取码：nc3o）](https://caiyun.139.com/m/i?2fALg7syUoC5n)

[macOS Monterey 12.6 iso 下载链接（提取码：pn3d）](https://caiyun.139.com/m/i?2fALgqtVuvpdh)

## 二、创建虚拟机

### （一）创建新的虚拟机

打开VMware Workstation Pro，点击创建新的虚拟机，选择典型(推荐)，当然自定义(高级)也可以，这些参数后期都是可以修改的。

![](https://cdn.luogu.com.cn/upload/image_hosting/s0e42uxg.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/gg1skc3w.png)

### （二）安装程序光盘映像文件

然后点击下一步，选择安装程序光盘映像文件(iso)，点击浏览选择我们下载好的光盘映像的位置，选择文件，打开文件，然后点击下一步。

![](https://cdn.luogu.com.cn/upload/image_hosting/7uibdma1.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/yz5rmz62.png)

### （三）选择客户机操作系统

然后就到了选择客户机操作系统，如果VMware在没有使用Unlocker解锁的情况下打开，在选择虚拟机操作系统时就没有Apple Mac OS X的选项。

版本我们选择iso文件的版本，这里我提供的是macOS Catalina 10.15.7，就选择macOS 10.15就可以了。

![](https://cdn.luogu.com.cn/upload/image_hosting/drfmd57z.png)

### （四）命名虚拟机

然后是命名虚拟机，这个自己决定就行了，好了之后点击下一步。

### （五）指定磁盘容量

最大磁盘大小填写 80GB 就够用了，我安装完之后发现系统大小大约是 20GB ，自己决定，别的设置都不用改，好了之后点击下一步。

![](https://cdn.luogu.com.cn/upload/image_hosting/4x3nikg9.png)

最后给虚拟机配置网络，点击自定义硬件，然后点击网络适配器，选择桥接模式：直接连接物理网络，然后点击关闭，点击完成。

![](https://cdn.luogu.com.cn/upload/image_hosting/k0dc6k84.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/8x0s89lk.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/z3owtve7.png)

## 三、安装macOS

### （一）开启虚拟机

点击开启此虚拟机，如果出现了一个白苹果，下面有一个进度条，则说明成功了。（如果打开显示Boot Manager，下面还有一系列选项，那说明镜像文件不支持你的CPU，只能换个镜像重新弄，目前发现AMD不支持，Intel可以）

![](https://cdn.luogu.com.cn/upload/image_hosting/3gbx0911.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/t0dguods.png)

### （二）抹掉磁盘

等待进度条跑满，直到白苹果消失，选择语言为中文，点击磁盘工具，看左边的内置栏，选择第一个硬盘，然后点击上方的抹掉。

![](https://cdn.luogu.com.cn/upload/image_hosting/6ffv8cb0.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/mo88iv6z.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/wwdmhs8l.png)

抹掉的名称自己随意，下面两个不改，然后点击抹掉。

![](https://cdn.luogu.com.cn/upload/image_hosting/ypw49s3m.png)

### （三）安装macOS

完成后点击左上角小红点，关闭磁盘工具，然后点击安装macOS，点击继续，点击同意，然后点击我们刚才抹掉的硬盘，点击继续，等待安装（大约 40 分钟）。

![](https://cdn.luogu.com.cn/upload/image_hosting/yexr6rhu.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/6rsxfn5e.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/50qr1dvk.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/ez6tx7ho.png)

### （四）配置macOS

然后就进入了配置界面。由于配置流程很长，配置过程就不配图了，一直点继续就可以了。

## 四、优化

安装的过程肯定是非常顺利的，但是当我们满心欢喜的打开系统时，发现在虚拟机下，拖动鼠标具有明显的掉帧现象，不能实现全屏也就是调节分辨率，也不支持传输文件。

### （一）安装VMware Tools

所以，我们需要在虚拟机里安装一个叫做VMware Tools的程序。

#### 1. 自动安装

下面两种安装方式任选其一即可。

-  点击左上方虚拟机选项卡，点击安装VMware Tools即可安装。
-  点击下方安装Tools。

![](https://cdn.luogu.com.cn/upload/image_hosting/gxdpfftm.png)

#### 2. 未显示自动安装/自动安装失败

这时就需要用到一个叫做darwin.iso的文件。

如果使用了Unlocker解锁VMware，Unlocker会自动帮你下载一个最新版的darwin.iso，并下载到unlocker<版本号>\iso的文件夹里，打开后你就会发现有一个darwin.iso。

![](https://cdn.luogu.com.cn/upload/image_hosting/g65oe5lm.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/cblo3wi6.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/ecfmho9h.png)

然后将你的虚拟机关机，点击编辑虚拟机设置，然后点击CD/DVD（SATA）把使用ISO映像文件指定为darwin.iso。

![](https://cdn.luogu.com.cn/upload/image_hosting/l40b73yg.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/68l3ogl4.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/3x3a2vsk.png)

启动虚拟机，在桌面右上角可以看到VMware Tools，双击打开。

![](https://cdn.luogu.com.cn/upload/image_hosting/3gbx0911.png)

![](https://cdn.luogu.com.cn/upload/image_hosting/h5wb9muq.png)

双击安装，然后跟随安装引导就可以了，所有的弹窗都点击允许。

最后重新启动，你就可以看到流畅的macOS系统了！

## 结言

到这里本篇教程就结束了，如果有错误的地方，也请dalao指出，有问题也可以在评论区/私信问作者~
