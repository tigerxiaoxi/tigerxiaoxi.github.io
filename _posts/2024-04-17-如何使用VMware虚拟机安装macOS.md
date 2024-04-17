---
layout:     post
title:      这篇教程教你在Windows电脑上安装macOS
subtitle:   让我们安装macOS吧
date:       2024-4-17
author:     TigerXiaoxi
header-img: img/the-first.png
catalog: false
tags:
    - Windows
---


# 使用VMware虚拟机软件安装macOS

需要：

- 虚拟机运行软件：VMware Workstation Pro（版本随意）
- VMware macOS解锁程序：Unlocker
- macOS系统镜像文件（ISO）

准备
------------

[VMware Workstation Pro网盘下载](https://caiyun.139.com/m/i?1A5Cvaun8nrql) 提取码:cv2A

因为VMware Workstation Pro是收费的，我这里有免费版，打包到网盘里给大家了（下载不限速，不像某度网盘）

下载好后解压，双击安装程序，一直点击下一步，到填写许可证的界面，点击<许可证>，许可证默认是填好的，点击<输入>，再点击<完成>就安装完了

如果VMware在没有使用Unlocker解锁的情况下打开，在选择虚拟机操作系统时没有Apple Mac OS X的选项

[unlocker官网](https://github.com/DrDonk/unlocker/releases)

点击↑链接下载Unlocker

在官网界面，有Unlocker的各个版本，找到最新版本，下面有一个Assets，点击Unlocker<版本号>.zip下载后先解压

工具使用之前要先关掉VMware，后台的VMware进程也要清理一空。右键开始键，选择“任务管理器”，然后往下滑，找到名字带有VMware的进程，全部都右键——结束进程。等一会儿，如果有“死而复生”的，也干掉它们，直到没有一个VMware进程为止

然后打开解压后的文件夹，打开windows文件夹，找到里面叫unlock.exe的程序，右键使用管理员身份运行，运行完之后关闭cmd就可以了

使用VMware配置
------------

然后打开VMware Workstation Pro，点击创建新的虚拟机，选择<典型(推荐)>，当然<自定义(高级)>也可以，这些参数后期都是可以修改的

然后点击下一步，选择<安装程序光盘映像文件(iso)>，点击<浏览>选择光盘映像(iso)的位置，双击文件选择，然后点击下一步

然后就到了选择客户机操作系统，如果VMware在没有使用Unlocker解锁的情况下打开，在选择虚拟机操作系统时没有Apple Mac OS X的选项

然后版本我们选择ISO文件的版本，这里我提供的是Sonoma macOS 14.4.1，就选择macOS 14就可以了

[macOS 14.4.1 ISO 网盘下载](https://cloud.189.cn/t/FBzAvazmaYvi) 访问码：afa7（这个也是特地找的不限速网盘）

然后到了命名虚拟机，这个自己决定就行了，好了之后点击<下一步>

最大磁盘大小填写80G就够用了，我安装完之后发现系统大小大约是20GB，自己决定，别的设置都不用改，好了之后点击<下一步>，然后点击<完成>虚拟机就设置完了

安装macOS
------------

然后点击<开启此虚拟机>，如果出现了一个白苹果，下面有一个进度条，则说明成功了（如果打开显示Boot Manager，下面还有一系列选项，那说明镜像文件不支持你的cpu，只能换个镜像重新弄，目前发现AMD不支持，Intel可以）

等待进度条跑满，直到白苹果消失，选择语言为中文，点击<磁盘工具>，看左边的<内置>栏，选择第一个硬盘，然后点击右上方的抹掉

抹掉的名称自己随意，下面两个不改，然后点击<抹掉>

完成后点击左上角小红点，关闭磁盘工具，然后点击<安装macOS "版本名">，点击<继续>，点击<同意>，然后点击我们刚才抹掉的硬盘，点击<继续>，等待安装（建议去看一集86版西游记，大概40分钟）

macOS配置
------------

然后终于进入了配置界面

选择国家和地区当然选择<中国大陆>，点击<继续>

语言与输入法不用改，直接点击<继续>

辅助功能点击<以后>

数据与隐私点击<继续>

迁移助理点击左下角的<以后>

使用你的Apple ID登录界面，登录你的Apple ID，没有的话注册一个，或者点击左下角的稍后设置

验证码界面自己输，如果没有已登录的苹果设备点下方的<没有收到验证码？>，点击发送验证短信，输入完后点击右下角的<验证>

创建电脑账户自己填，提示不用填，密码不能跟Apple ID密码一样，好了之后点击右下角<继续>

快捷设置点击<继续>

如果不想让自己的个人信息被Apple知道的话，分析不打钩，点击右下角的<继续>

屏幕使用时间都不动，点右下角<继续>

iCloud分析一样，不打钩，点右下角<继续>

Siri自己选，点右下角<继续>

选择Siri语言自己选（如果想听听Siri是怎么将粤语的，可以选下面那个，我没听过），<继续>

改进Siri与听写推荐选<以后>，<继续>

选取您的外观按自己口味选择，<继续>

等待设置您的Mac，配置完成！

最后终于见到了Mac桌面


优化
------------
### 准备

安装的过程想必非常顺利的，但是当我们满心欢喜的打开系统时，发现在虚拟机下，拖动鼠标具有明显的掉帧现象，不能实现全屏也就是调节分辨率，也不支持传输文件

所以，我们需要安装在虚拟机里安装一个叫做VMware Tools的软件

安装VMware Tools需要用到一个叫做darwin.iso的文件（没错，是光盘映像）

如果是使用了unlocker解锁VMware，unlocker会自动帮你下载一个最新版的darwin.iso，并下载到unlocker<版本号>\iso的文件夹里，打开后你会发现就有一个darwin.iso

如果官方源不稳定，可能会失效，有时候需要我们手动安装：

可以在这个网站上下载：[darwin.iso官网下载](http://softwareupdate.vmware.com/cds/vmw-desktop/fusion/)

找到最新的版本号（以13.5.1为例），点击<13.5.1（最新版本）>\<23298085>\<universal>\<core>，这时候到了file页面，下载第一个<com.vmware.fusion.zip.tar>，下载完后解压.tar，解压完后点开文件夹再解压.zip，最后就是com.vmware.fusion文件夹了，darwin.iso在这个路径下：

```
com.vmware.fusion\payload\VMware Fusion.app\Contents\Library\isoimages\x86_x64
```
### 安装

将你的虚拟机关机，点击<编辑虚拟机设置>，然后点击<CD/DVD(SATA)>把使用ISO映像文件指定为darwin.iso

启动虚拟机，在桌面右上角可以看到VMware Tools，双击打开

双击安装，然后跟随安装引导就可以了，记住，所有的弹窗都点击<允许>

最后重新启动，你就可以看到顺畅的macOS系统，赶紧全屏，体验一下macOS吧！

结言
------------
创建我的个人博客耗费了两周的时间和巨大的精力，写这篇博客耗费了3天的时间，最终完稿日期：2024.4.17，希望看到的人能分享这个网站，之后我会更新更多的内容！谢谢大家！
<!-- Gitalk end -->

 <!-- disqus 评论框 start  -->
{% if site.disqus.enable %}

<div class="comment">
    <div id="disqus_thread" class="disqus-thread">
    </div>
</div>
<!-- disqus 评论框 end -->

<!-- disqus 公共JS代码 start (一个网页只需插入一次) -->
<script type="text/javascript">
    /* * * CONFIGURATION VARIABLES * * */
    var disqus_shortname = "{{site.disqus.username}}";
    var disqus_identifier = "{{site.disqus.username}}/{{page.url}}";
    var disqus_url = "{{site.url}}{{page.url}}";

    (function() {
        var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
        dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
        (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
    })();
</script>
<!-- disqus 公共JS代码 end -->
{% endif %}
