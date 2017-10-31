title: 学习Swift写iOS?那写安卓和WinPhone呢？请看一石三鸟终极解决方案 - Silver！
tags:
  - Silver
  - Swift
  - 跨平台
id: 538
categories:
  - Hacker News
  - Swift
date: 2015-02-09 16:08:00
---

<div id="article_content" class="article_content">&#13;

![](http://img.blog.csdn.net/20150209154637248?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<span style="color: rgb(51, 102, 255);">首先，你必须知道的是，Silver是苹果最新编程语言[Swift](http://www.apple.com/swift)的免费实现版本。</span>

<span style="color: rgb(51, 102, 255);">通过Silver，你可以使用Swift语言来编写.NET，Java，安卓和Cocoa APIs。你甚至可以在这些平台上共享大部分的非UI部分的代码。</span>

<span style="color: rgb(51, 102, 255);">
</span>
<div class="page" style="vertical-align: top; font-family: myriad-pro, 'Lucida Grande', 'Segoe UI', 'Lucida Sans Unicode', sans-serif; font-size: 16px; line-height: 20.7999992370605px;">

# <span style="color: rgb(51, 102, 255);">获得<span style="font-size: 20pt; line-height: 20.7999992370605px;">Beta版本</span></span>
</div><div style="font-family: myriad-pro, 'Lucida Grande', 'Segoe UI', 'Lucida Sans Unicode', sans-serif; font-size: 16px; line-height: 20.7999992370605px; border: 1px solid rgb(192, 192, 192); margin-bottom: 25px; padding: 10px 10px 0px; width: 595px; margin-left: -10px; background-color: rgb(240, 240, 240);"><div class="page" style="vertical-align: top;">

<span style="color: rgb(51, 102, 255); font-size: 14pt; line-height: 1.4em;">Silver当前还处于Beta公测阶段，但是已经是非常可用的状态了。请在下面提供你的email，我们就会立即为你注册访问权限。这可是免费的哦！</span>
</div><form role="form" class="form-inline" method="post" style="margin: 0px; padding: 0px; font-size: 14pt; line-height: 1.4em;"><table cellpadding="0" cellspacing="10" class="  " style="margin-left: auto; margin-right: auto;"><tbody><tr><td align="left" style="font-family: myriad-pro, 'Lucida Grande', 'Segoe UI', 'Lucida Sans Unicode', sans-serif; font-size: 16pt; line-height: 1.3em;"><label for="emailAddress"><span style="color: rgb(51, 102, 255);">名称：</span></label></td><td align="left" style="font-family: myriad-pro, 'Lucida Grande', 'Segoe UI', 'Lucida Sans Unicode', sans-serif; font-size: 16pt; line-height: 1.3em;"><input name="name" id="fullnameField" placeholder="Enter your name" autocorrect="off" value="" size="25" autocomplete="name-full" style="font-size: 20pt; line-height: 1.4em;" /></td></tr><tr><td align="left" style="font-family: myriad-pro, 'Lucida Grande', 'Segoe UI', 'Lucida Sans Unicode', sans-serif; font-size: 16pt; line-height: 1.3em;"><label for="emailAddress"><nobr><span style="color: rgb(51, 102, 255);">邮件地址：</span></nobr></label></td><td align="left" style="font-family: myriad-pro, 'Lucida Grande', 'Segoe UI', 'Lucida Sans Unicode', sans-serif; font-size: 16pt; line-height: 1.3em;"><input name="emailAddress" type="email" placeholder="Enter your email address" value="" size="25" autocomplete="email" style="font-size: 20pt; line-height: 1.4em;" /></td></tr><tr><td align="center" colspan="2" style="font-family: myriad-pro, 'Lucida Grande', 'Segoe UI', 'Lucida Sans Unicode', sans-serif; font-size: 12pt; line-height: 1.3em;"><input type="submit" value="Get the Silver Beta" style="font-size: 12pt; line-height: 1.4em; padding: 5px; border: 1px solid rgb(192, 192, 192); border-radius: 5px; color: rgb(64, 64, 64); background-color: rgb(224, 224, 224);" /></td></tr></tbody></table><span style="color:#ff0000;">天地会珠海分舵注:请英文不好的童鞋参考这表单的翻译，然后到原文链接去填写，不要真的在这篇文章中填写点击。</span></form></div>

# <span style="color:#3366ff;">背景</span>

<span style="color: rgb(51, 102, 255);">在拥有十多年强悍的编译器知识和技术积累的基础上构建出来的Silver是一个真实的原声的Swift的编译器，它可以为.NET CLR，Java/Android JVM和Cocoa运行时提供编译工作。</span>

<span style="color: rgb(51, 102, 255);">Silver支持3个平台，但要注意的是它一开始就非常明确的定位在非跨平台方向的，它关注的方向是让你在各个平台上利用Swift语言以原生的方式来编写应用，而不是鼓励大家想其他烂大街的框架一样去利用它来编写跨平台的应用。使用Silver的同时，你可以复用你的语言技术和专业工具技能，而同时你还可以复用你编写的大量的后台业务逻辑 - 但你将会使用它来在各个独立的目标平台上编写应用。[为什么](http://elementscompiler.com/native)？因为伟大的应用都是这样写出来的。</span>

# <span style="color: rgb(51, 102, 255);">开发环境</span>

<span style="color: rgb(51, 102, 255);">Silver其实不仅仅是一个编译器，它同时也是开发移动应用的<span style="font-size: 18.6666660308838px; line-height: 26.1333332061768px;">一个完整</span>的工具链和开发环境。</span>

<span style="color: rgb(51, 102, 255);">对于一直在Windows上进行开发的开发人员来说，Silver深深的集成在微软的顶尖IDEs - Visual Studio 2013和2015里面。</span>

<span style="color: rgb(51, 102, 255);">对于一直在Mac上进行开发的开发人员来说，Silver给你带来了[Fire](http://elementscompiler.com/elements/fire)，这是属于我们自己的一套开发环境，它完全是为了给Mac上的元素/组件进行编译和创建出轻量级，高产的应用而由我们自主研发的一套开发框架。</span>

# <span style="color: rgb(51, 102, 255);">文档</span>

<span style="color: rgb(51, 102, 255);">如需深入查看Silver相关的文档请访问[docs.elementscompiler.com/Silver](http://docs.elementscompiler.com/Silver)<span style="font-size: 18.6666660308838px; line-height: 26.1333332061768px;">.</span></span>

---------------------------------------完---------------------------------------------------

英文原文参考链接：[http://elementscompiler.com/elements/silver/](http://elementscompiler.com/elements/silver/)

<table border="1" cellspacing="0" cellpadding="0"><tbody><tr><td valign="top" style="background: rgb(250, 191, 143);">

**<span style="color: rgb(54, 46, 43);">作</span><span style="color: rgb(54, 46, 43);">/译者</span>**
</td><td valign="top" style="background: rgb(250, 191, 143);">

**<span style="color: rgb(54, 46, 43);">微信知识共享公众号</span>**
</td><td valign="top" style="background: rgb(250, 191, 143);">

**<span style="color: rgb(54, 46, 43);">CSDN</span>**
</td></tr><tr><td valign="top" style="background: rgb(227, 228, 228);">

<span style="color: rgb(54, 46, 43);">天地会珠海分舵</span>
</td><td valign="top">

<span style="color: rgb(54, 46, 43);">TechGoGoGo</span>
</td><td valign="top">

<span style="color: rgb(54, 46, 43);">http://blog.csdn.net/zhubaitian</span>
</td></tr><tr><td valign="top" style="background: rgb(251, 212, 180);">

<span style="color: rgb(54, 46, 43);">优秀资源推荐</span>
</td><td valign="top" style="background: rgb(251, 212, 180);">

<span style="color: rgb(54, 46, 43);">地址</span>
</td><td valign="top" style="background: rgb(251, 212, 180);">

<span style="color: rgb(54, 46, 43);">点评</span>
</td></tr><tr><td valign="top" style="background: rgb(227, 228, 228);">

<span style="color: rgb(54, 46, 43);">DoctorQ</span><span style="color: rgb(54, 46, 43);">博客</span>
</td><td valign="top">

<span style="color: rgb(54, 46, 43);">[<span style="color: rgb(106, 57, 6);">http://testerhome.com/doctorq/topics</span>](http://testerhome.com/doctorq/topics)</span>
</td><td valign="top">

<span style="color: rgb(54, 46, 43);">安卓自动化领域才俊</span><span style="color: rgb(54, 46, 43);">           </span>
</td></tr><tr><td valign="top" style="background: rgb(227, 228, 228);">

<span style="color: rgb(54, 46, 43);">金阳光测试</span>
</td><td valign="top">

<span style="color: rgb(54, 46, 43);">官网：</span><span style="color: rgb(54, 46, 43);">[www.goldensunshine.cc](http://www.goldensunshine.cc/)</span>
</td><td valign="top">

<span style="color: rgb(54, 46, 43);">更多请百度搜：“金阳光”</span>
</td></tr></tbody></table></div>