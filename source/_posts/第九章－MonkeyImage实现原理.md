title: 《MonkeyRunner原理剖析》第九章－MonkeyImage实现原理 - 概览
id: 231
categories:
  - 技术
date: 2015-01-24 14:54:04
tags:
---

MonkeyRunner没有引进Junit等单元测试框架，所以没有相应的断言方法来去对测试结果进行判断。<!--more-->

<span class="s1"> 但MonkeyRunner提出了另外一个判断执行结果成功与否的方法，那就是通过截图比对。毕竟MonkeyRunner是对UI进行自动化测试的框架，所以通过截屏来对结果进行比对还是靠谱的。</span>

<span class="s1"> MonkeyRunner提供了跟MonkeyDevice同层级的MonkeyImage类来专门处理截图相关的操作，本章会对其实现原理进行深入的阐述。</span>

<table class="      xhe-border" width="539" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td valign="top" width="111" height="13">作者</td>
<td valign="top" width="112" height="13">自主博客</td>
<td valign="top" width="111" height="13">微信</td>
<td valign="top" width="112" height="13">CSDN</td>
</tr>
<tr>
<td valign="top" width="111" height="39">天地会珠海分舵</td>
<td valign="top" width="112" height="39"><span class="Apple-style-span">[http://techgogogo.com](http://techgogogo.com/)</span></td>
<td valign="top" width="111" height="39">服务号<span class="Apple-style-span">:TechGoGoGo</span>扫描码<span class="Apple-style-span">:</span></td>
</tr>
</tbody>
</table>
![](http://mmbiz.qpic.cn/mmbiz/KYJTqcL56vuJuQArNAk7nsLW8hpxia6kjor2IEvib9RAQTEzzEPa4UngfjpT1GKIIKCnb7ib0IViaWEV7VFFiaAkkjg/640?tp=webp)<span class="Apple-style-span">[http://blog.csdn.net/zhubaitian](http://blog.csdn.net/zhubaitian)</span>