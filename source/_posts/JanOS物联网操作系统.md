title: 国内首篇介绍JanOS物联网操作系统的文章 - 如何把你的手机主板打造成物联网
tags:
  - IoT
  - JanOS
  - 操作系统
  - 树莓派
  - 物联网
id: 528
categories:
  - Hacker News
date: 2015-02-12 09:24:00
---

<div id="article_content" class="article_content">&#13;

<span style="color: rgb(255, 0, 0);"><span style="font-size: 18px;">**天地会珠海分舵注**</span>:如无意外，您现在正在看的将是国内首篇且是唯一一篇介绍炙手可热的物联网的操作系统**<span style="font-size: 24px;">[JanOS](http://janos.io/)</span>**的文章！不信你去百度！希望大家能喜欢。但本文只是引言，更多信息请还是访问JanOS的官网：[http://janos.io/](http://janos.io/)</span>

![](http://img.blog.csdn.net/20150211221349878?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![](http://img.blog.csdn.net/20150211221445836?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<span style="font-size: 48px; color: rgb(153, 51, 0);">JanOS</span>

<span style="font-size: 32px; color: rgb(255, 204, 102);">让你的手机瞬间变身成物联网平台</span>
> <span style="font-size: 18px;">JanOS是一个设计成运行在你的手机芯片上的操作系统。它可以在没有屏幕的情况下跑起来，让你可以可以通过当今红得发紫的JavaScript的API来访问你的手机的所有功能，从打电话到照相功能无所不包。</span>

![](http://img.blog.csdn.net/20150211222014822?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<span style="font-size: 24px;">你问我在搞毛?</span>
> <span style="font-size: 18px;">当前炙手可热的物联网解决方案开发版存在一个重大的问题是：一个字“贵！”(天地会珠海分舵注：别跟我算标点符号哦)，两个字"很贵!"，三个字"非常贵！"，四个字"一斤切糕!"，五个字"一个茶叶蛋!"。你看，像树莓派和阿都伊诺这些仅仅只是提供了有限功能集和简单扩展如GSM Shield等的就能卖到80美刀。着对于坐拥”十斤切糕”的你也许不算什么，但是对于我们这些只有十个雪糕的财富值的人就不一样了，因为相比一个提供了完整功能的智能手机只卖个30美刀，该价格可以下死个人了。所以为什么不把你那值几个雪糕的智能手机主板改装成一个物联网平台来进行嵌入式项目开发呢？几个雪糕就能换来强大的功能，何乐而不为呢？</span>

![](http://img.blog.csdn.net/20150211223704724?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<span style="font-size: 32px;">入门指南</span>

1.  <span style="font-size: 18px;">首先根据我们的[支持设备列表](http://janos.io/device-list.html)来花几个雪糕的价格搞一个智能手机吧</span>
2.  <span style="font-size: 18px;">获取一个[现成JanOS版本](http://janos.io/download.html)，或者[构建一个你自己的JanOS版本](http://janos.io/device-list.html#how-to-build)</span>
3.  <span style="font-size: 18px;">克隆我们的[应用模版](http://github.com/jan-os/janos)和编写你的[第一个程式](http://janos.io/articles/first-app.html)</span>
4.  <span style="font-size: 18px;">运行命令<span style="font-family: 'Open Sans', sans-serif; line-height: 28.7999992370605px;"> </span><span class="code" style="font-family: monospace; padding: 0.3rem; border-radius: 0.3rem; line-height: 28.7999992370605px; background: rgb(238, 238, 238);">make reset-phone</span><span style="font-family: 'Open Sans', sans-serif; line-height: 28.7999992370605px;"> 来更新你的设备</span></span>
5.  <span style="font-family: 'Open Sans', sans-serif; font-size: 18px;"><span style="line-height: 28.7999992370605px;">当一节就绪后，[拧开你的智能手机](http://youtu.be/Uy062kp-LM4?t=5m11s)并把主板解体出来</span></span>
6.  <span style="font-family: 'Open Sans', sans-serif; font-size: 18px;"><span style="line-height: 28.7999992370605px;">随便你用你的主板来搞成什么东东</span></span>
7.  <span style="font-family: 'Open Sans', sans-serif; font-size: 18px;"><span style="line-height: 28.7999992370605px;">为你在这个过程中的收获惊呼吧!</span></span><div><span style="font-family: 'Open Sans', sans-serif; font-size: 18px;"><span style="line-height: 28.7999992370605px;">![](http://img.blog.csdn.net/20150211224752811?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
</span></span></div><div><span style="font-family: 'Open Sans', sans-serif; font-size: 32px;"><span style="line-height: 28.7999992370605px;">**常见问题**</span></span></div><div>

*   <span style="font-size: 18px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;"> **我可以在上面挂个传感器或LED吗？**</span><span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">大部分的手机都有一些</span>[GPIO金手指 ](http://en.wikipedia.org/wiki/General-purpose_input/output)<span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">来让你挂载一些额外的电子原件到其主板上面，比如LED灯等。我们之前刊登了一个</span>[博客文章](http://ee.telenor.io/gonzo/hardware/2015/02/10/gpio.html)<span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">来描述如何把一个LED挂载到</span><span style="line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif; font-size: 14px;">GeeksPhone Keon火狐手机上并对其进行控制。</span>
*   <span style="line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;"><span style="font-size: 18px;">这东东可以跑原生代码不？</span></span><span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">你可以用Android NDK/工具链为该ARM架构的主板编译任何C/C++的二进制代码，并可以使用</span>[mozOs.exec](http://janos.io/api-reference/exec.html)<span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;"> </span><span style="line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif; font-size: 14px;">API来对该二进制代码进行调用。请点击查看[示例](http://janos.io/articles/cross-compile.html)。</span>
*   <span style="line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;"><span style="font-size: 18px;">哥，这玩意儿省电不？</span></span><span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">这就要看你是如何用你的手机了。总的来说，在空闲状态的2G网络下消耗的大概是5-10mA每小时的电量。你可以试下用个电子USB安培计来检查下真是的电量消耗情况了。</span>[更多信息请看这里](https://hacks.mozilla.org/2014/04/measuring-power-consumption-on-phones/)<span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">。</span>
*   <span style="line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;"><span style="font-size: 18px;">这家伙要电池不？</span></span><span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">妖！你见过不用电池就能跑大多应用(启动,wifi网络检测之类)的手机吗？当然要电池了。接个电池还不容易吗。毫不费力的在你的几个雪糕的</span>[主板背后](http://janos.io/img/gonzo-worked-open.jpg)<span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">焊个电池不就完了嘛。</span>
*   <span style="line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;"><span style="font-size: 18px;">介绍个调试器用用呗？</span></span><span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">用</span>[WebIDE](http://janos.io/articles/first-app.html#debugger)<span style="font-size: 14px; line-height: 28.7999992370605px; font-family: 'Open Sans', sans-serif;">吧，这是Firefox开发工具的一部分了，专门用来连接你的设备进行调试的。</span><div><span style="font-family: 'Open Sans', sans-serif; font-size: 14px;"><span style="line-height: 28.7999992370605px;">－－－－－－完－－－－－－－－－－</span></span></div><div><span style="font-family: 'Open Sans', sans-serif; font-size: 14px;"><span style="line-height: 28.7999992370605px;"></span></span><table border="1" cellspacing="0" cellpadding="0" style="color: rgb(54, 46, 43); font-family: Arial; font-size: 14px; line-height: 26px;"><tbody><tr><td valign="top" style="background: rgb(250, 191, 143);">

**作/译者**
</td><td valign="top" style="background: rgb(250, 191, 143);">

**微信知识共享公众号**
</td><td valign="top" style="background: rgb(250, 191, 143);">

**CSDN**
</td></tr><tr><td valign="top" style="background: rgb(227, 228, 228);">

天地会珠海分舵
</td><td valign="top">

TechGoGoGo
</td><td valign="top">

http://blog.csdn.net/zhubaitian
</td></tr><tr><td valign="top" style="background: rgb(251, 212, 180);">

优秀资源推荐
</td><td valign="top" style="background: rgb(251, 212, 180);">

地址
</td><td valign="top" style="background: rgb(251, 212, 180);">

点评
</td></tr><tr><td valign="top" style="background: rgb(227, 228, 228);">

DoctorQ博客
</td><td valign="top">

[http://testerhome.com/doctorq/topics](http://testerhome.com/doctorq/topics)
</td><td valign="top">

安卓自动化领域才俊 
</td></tr></tbody></table>
</div><span style="font-family: 'Open Sans', sans-serif;"><span style="line-height: 28.7999992370605px;"></span></span></div></div>