title: 且看如何以精致的方式展现，解析和分析GitHub上语言的发展趋势
tags:
  - GitHub
  - GitHut
  - 大数据
  - 编程语言
id: 526
categories:
  - Hacker News
date: 2015-02-12 16:41:00
---

<div id="article_content" class="article_content">&#13;

GitHut网站原文连接:[http://githut.info/](http://githut.info/),其实这是一个非常简单的只有一个页面的网站。做的事情就是去通过GitHub Archive来获取到GitHub代码仓库的大数据然后进行分析，并把Github上用到的各种语言的信息整理出来并呈现给大家。

![](http://img.blog.csdn.net/20150211191204646?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

##### GITHUT

_<span style="color: rgb(102, 102, 102);">GitHut is an attempt to visualize and explore the complexity of the universe of programming languages used across the repositories hosted on GitHub.</span>_

<span style="color: rgb(51, 102, 255);">Githut尝试通过分析和探索Github上的大量的错综复杂的项目所用到的编程语言来把它们呈现出来给大家，以便大家更容易把握当前流行语言的走向和趋势。</span>
<span style="color: rgb(153, 153, 153);">_
Programming languages are not simply the tool developers use to create programs or express algorithms but also instruments to code and decode creativity. By observing the history of languages we can enjoy the quest of human kind for a better way to solve problems, to facilitate collaboration between people and to reuse the effort of others._</span>

<span style="color: rgb(51, 102, 255);">编程语言不仅仅是我们所认知的给程序员用来创建应用和实现算法的一个工具，同时它里面还封装和透露着人类伟大创造力的气息。通过观察语言的发展历史，我们很欣慰我们人类一直在追求着更优的解决问题的方法，以让人们之间的协作变得更加方便和让我们可以复用别人的努力成功而减少人力资源的浪费。</span>

<span style="color: rgb(153, 153, 153);">_[Github](http://githut.info/#) is the largest code host in the world, with 3.4 million users. It's the place where the open-source development community offers access to most of its projects. By analyzing how languages are used in GitHub it is possible to understand the popularity of programming languages among developers and also to discover the unique characteristics of each language. _</span>

[Github](http://githut.info/#)<span style="color: rgb(51, 102, 255);">是世界上存有代码量最大的地方，它拥有者340万的用户量。这是一个开源开发社区提供大部分它们的项目让大家进行访问的地方。通过分析GitHub上的开发语言使用情况就很容易可以去了解开发人员当今正在使用的开发语言的流行程度以及这些语言各自的特性。</span>

##### DATA

_<span style="color: rgb(153, 153, 153);">GitHub provides publicly available [API](http://githut.info/#) to interact with its huge dataset of events and interaction with the hosted repositories.</span>_

GitHub提供了公共API来跟其巨大的事件数据集以及里面的代码仓库进行互动。

<span style="color: rgb(153, 153, 153);">_[GitHub Archive](http://www.githubarchive.org/) takes this data a step further by aggregating and storing it for public consumption. GitHub Archive dataset is also available via [Google BigQuery](https://developers.google.com/bigquery/). 
The quantitative data used in GitHut is collected from [GitHub Archive](http://www.githubarchive.org/). The data is updated on a quarterly basis._</span>

[GitHub Archive](http://www.githubarchive.org/)<span style="color: rgb(17, 17, 17);"> </span><span style="color: rgb(51, 102, 255);">更进一步的把这些巨大的数据聚合并保存起来提供公共服务。Github Archive数据集同时也可以通过</span><span style="color: rgb(17, 17, 17);"> </span>[Google BigQuery](https://developers.google.com/bigquery/)<span style="color: rgb(51, 102, 255);">来获得。我们这里GitHut所用到的计量数据就是通过</span>[GitHub Archive](http://www.githubarchive.org/)<span style="color: rgb(17, 17, 17);"> </span><span style="color: rgb(51, 102, 255);">来收集到的。这些数据会在每个季度进行更新。</span>

_<span style="color: rgb(153, 153, 153);">An additional note about the data is about the large amount of records in which the programming language is not specified. This particular characteristic is extremely evident for the Create Events (of repository), therefore it is not possible to visualize the trending language in terms of newly created repositories. For this reason the Activity value (in terms of number of changes pushed) has been considered the best metric for the popularity of programming languages. </span>_

<span style="color: rgb(51, 102, 255);">另外，对于我们获得的这些数据值得一提的一点是，其实GitHub Archive上面还有大量的数据里面是没有编程语言相关的信息的。这在先创建一个代码仓库所产生的创建事件中表现的特别明显(</span><span style="color: rgb(255, 0, 0);">天地会珠海分舵注:因为创建一个仓库跟你创建一个文件夹来存放代码差不多，你没有存放实际的代码，我们怎么知道你这个仓库会用到什么编程语言呢？</span><span style="color: rgb(51, 102, 255);">)，因此，我们是没有办法去根据新创建的代码仓库来分析编程语言的发展趋势的。鉴于这个原因，我们去分析开发语言流行度最好的角度就是去分析那些代码改变后的签入相关的事件信息了。</span>
<span style="color: rgb(153, 153, 153);">_
The release year of the programming language is based on the table [Timeline of programming languages](http://en.wikipedia.org/wiki/Timeline_of_programming_languages) from Wikipedia. _</span>

<span style="color: rgb(51, 102, 255);">上面的图表所现实的各种开发语言的发布日期参照的是Wikipedia上的</span>[开发语言时间轴](http://en.wikipedia.org/wiki/Timeline_of_programming_languages)<span style="color: rgb(51, 102, 255);">这个表。</span>

_<span style="color: rgb(153, 153, 153);">For more information on the methodology of the data collection check-out the publicly available GitHub [repository of GitHut](https://www.github.com/littleark/githut/).</span>_

<span style="color: rgb(51, 102, 255);">更多关于这些数据获取方式的信息请签出GitHub上公开的</span>[GitHut仓库](https://www.github.com/littleark/githut/)<span style="color: rgb(17, 17, 17);">。</span>

－－－－－－－完－－－－－－－－－－
<table border="1" cellspacing="0" cellpadding="0" style="color: rgb(54, 46, 43); font-family: Arial; font-size: 14px; line-height: 26px;"><tbody><tr><td valign="top" style="background: rgb(250, 191, 143);">

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
</td></tr></tbody></table></div>