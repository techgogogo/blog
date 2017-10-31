title: 还在等待漫长的iOS构建过程？来试试通过命令行的方式进行iOS应用快速构建和运行吧
tags:
  - ios
  - 命令行
  - 项目构建
id: 540
categories:
  - Hacker News
date: 2015-02-08 16:20:00
---

<div id="article_content" class="article_content">&#13;

<span style="font-size: 14px;">![](http://img.blog.csdn.net/20150208161849933?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
</span>

<span style="font-size: 14px;">不必多言，Xcode慢得很是众所周知的了。更甚者是，我有时发觉自己太依赖于Cocoa Touch的自动完成功能了，这可是个天使和魔鬼的结合体！</span>

故此我开始去寻觅一个替代的流程来通过命令行来实现我需要的功能。结果是相当让人困惑：有一些文章建议用xctool和xcodebuild来构建Xcode目标应用，然后用ios-sim,simctrl和instruments来管理和运行模拟器，但大部分这些信息都是老掉牙且零碎不堪的。

值得庆幸的是，我最终还是通过九牛二虎之力把这些琐碎的信息拼凑再一起来达到我自己的目的。那就是，假如现在有一个通过Xcode 6建立的iOS项目，我想要做到如下几点：

1.  构建目标应用
2.  启动一个iOS模拟器
3.  把该app应用安装到上面启动好的模拟器上面
4.  运行安装好的app
5.  从模拟器上卸载掉该app

那么我想把这些所有事情都通过命令行来实现，也就是说把Xcode给关闭掉的情况来完成这些工作。

在我们继续往下走之前，你需要先收集以下的一些基本信息：

1.  你所选择的通过Xcode进行构建的scheme(比如“AwesomeApp")
2.  你的应用包id(比如"com.awesome.app")
3.  已经创建好的模拟器的名称(比如"iPhone6 Plus")。如果你不想从Xcode的GUI中获取到这些信息，你大可以通过查看命令xcrun simtl list的输出来进行收集

准备好了吗？那我们就开始吧！

(注意以下的命令需要在你的项目文件夹下面运行)

构架目标应用：

    xcodebuild -scheme AwesomeApp -destination 'platform=iphonesimulator,name=iPhone 6 Plus' -derivedDataPath build`</pre>

    启动运行模拟器：
    <pre style="margin-top: 0px; margin-bottom: 10px; box-sizing: border-box; font-family: Monaco, Menlo, Consolas, 'Courier New', monospace; font-size: 13px; white-space: pre-wrap; padding: 9.5px; line-height: 1.428571429; color: rgb(51, 51, 51); word-break: break-all; word-wrap: break-word; border: 1px solid rgb(204, 204, 204); border-radius: 4px; background: rgb(245, 245, 248);">`xcrun instruments -w 'iPhone 6 Plus'`</pre>

    安装应用包(当然你是需要在通过以上命令构建好目标应用和启动完成模拟器之后来运行此命令了)
    <pre style="margin-top: 0px; margin-bottom: 10px; box-sizing: border-box; font-family: Monaco, Menlo, Consolas, 'Courier New', monospace; font-size: 13px; white-space: pre-wrap; padding: 9.5px; line-height: 1.428571429; color: rgb(51, 51, 51); word-break: break-all; word-wrap: break-word; border: 1px solid rgb(204, 204, 204); border-radius: 4px; background: rgb(245, 245, 248);">`xcrun simctl install booted build/Build/Products/Debug-iphonesimulator/AwesomeApp.app`</pre>

    启动模拟器中已经安装好的应用(在该应用已经通过如上命令安装好之后)
    <pre style="margin-top: 0px; margin-bottom: 10px; box-sizing: border-box; font-family: Monaco, Menlo, Consolas, 'Courier New', monospace; font-size: 13px; white-space: pre-wrap; padding: 9.5px; line-height: 1.428571429; color: rgb(51, 51, 51); word-break: break-all; word-wrap: break-word; border: 1px solid rgb(204, 204, 204); border-radius: 4px; background: rgb(245, 245, 248);">`xcrun simctl launch booted com.awesome.app
    `</pre>

    删除该安装包：
    <pre style="margin-top: 0px; margin-bottom: 10px; box-sizing: border-box; font-family: Monaco, Menlo, Consolas, 'Courier New', monospace; font-size: 13px; white-space: pre-wrap; padding: 9.5px; line-height: 1.428571429; color: rgb(51, 51, 51); word-break: break-all; word-wrap: break-word; border: 1px solid rgb(204, 204, 204); border-radius: 4px; background: rgb(245, 245, 248);">`xcrun simctl uninstall booted com.awesome.app

<span style="font-size: 14px;">如果你需要构建的是一个相当复杂的项目的话，你其实是需要给构建命令指定不少的一些参数的。具体请阅读RTFMs(Read The Fucking Manuals:阅读那该死的使用手册！)。如果你是像我一样是个懒虫的话，请通过编写一些脚本来自动完成这些步骤吧。</span>

<span style="font-size: 14px;">
</span>

<span style="font-size: 14px;">－－－－－－－－－－－完－－－－－－－－－－－－－－－－－－</span>

英文原文：[http://dduan.net/post/2015/02/build-and-run-ios-apps-in-commmand-line/](http://dduan.net/post/2015/02/build-and-run-ios-apps-in-commmand-line/)
<table border="1" cellspacing="0" cellpadding="0" style="color: rgb(54, 46, 43); font-family: Arial; font-size: 14px; line-height: 26px;"><tbody><tr><td valign="top" style="background: rgb(250, 191, 143);">

**转载请尊重原创/译**
</td><td valign="top" style="background: rgb(250, 191, 143);">

**微信公众号**
</td><td valign="top" style="background: rgb(250, 191, 143);">

**CSDN**
</td></tr><tr><td valign="top" style="background: rgb(227, 228, 228);">

**天地会珠海分舵**
</td><td valign="top">

服务号:TechGoGoGo
</td><td valign="top">

<u>http://blog.csdn.net/zhubaitian</u>
</td></tr><tr><td valign="top" style="background: rgb(251, 212, 180);">

**优秀资源推荐**
</td><td valign="top" style="background: rgb(251, 212, 180);">

**地址**
</td><td valign="top" style="background: rgb(251, 212, 180);">

**点评**
</td></tr><tr><td valign="top" style="background: rgb(227, 228, 228);">

DoctorQ博客
</td><td valign="top">

[http://testerhome.com/doctorq/topics](http://testerhome.com/doctorq/topics)

</td><td valign="top">

安卓自动化领域才俊，技术分享先驱，
</td></tr></tbody></table></div>