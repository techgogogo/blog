title: 当今最流行的Node.js应用开发框架简介
id: 508
categories:
  - Hacker News
date: 2015-02-24 10:50:00
tags:
---

<div id="article_content" class="article_content">&#13;
        <div class="markdown_views">

![这里写图片描述](http://img.blog.csdn.net/20150224095025117)

快速开发而又容易扩展，高性能且鲁棒性强。Node.js的出现让所有网络应用开发者的这些梦想成为现实。但是，有如其他新的开发语言技术一样，从头开始使用Node.js的最基本功能来编写代码构建应用是一个非常划不来的耗时的事情。这个问题的解决方案非常简单且已经经受起时间的考验：使用一个已经提前打造好的开发框架。因此才会有如此多的如Express.js，Koa，Sails.js等框架的概念提出来并加以实现。

这些开发框架的角色非常简单。就是要去为应用开发人员节省时间，让我们不用话费太多精力在一些不必要的事情上面。一旦一个框架可以满足开发人员的“用最小的代价来获得同样的产出”的理念的话，该框架就可以大行其道起来。

在当今的Node.js界中还没有一个框架可以一统江湖，虽然Express.js依然是迄今为止最流行的框架。但当今江湖上还有很多其他的门派在争夺武林盟主之位。不能说你丐帮成员众多别人就非要加入你丐帮的，大家都是为了学个防身之术(快速开发等Node.js框架)，你丐帮有降龙十八掌(Express.js)，人家武当还有太极(Sails.js等)啦。

总体来说你可以将Node.js开发框架归结为两类： 

 - 精简型框架  

 - 全栈型框架

下面我们就对这两种框架进行探讨。

# 精简型框架

精简型框架提供的是最基本的功能和APIs，这类框架本身就是被设计成用来改善Node.js开发过程中的主要方面的。但是，这些框架主要关注的方向都是提供基本的MVC开发框架功能和改善编码体验，而不是Node.js本身没有的其他功能和技术的支持。下面是一些当今流行的精简型的Node.js框架。

### Express.js- 最流行的框架

* * *

Express.js毫无疑问是当今最受网络应用开发人员喜爱的Node.js开发框架了。作为一个有弹性的，轻量级的，容易使用框架，Express.js完全可以用来开发纯JS或混合型的便于扩展的移动应用。如果网上一些数据不是空穴来风的话，当今世上已经有26000个网络和移动应用是使用该框架进行开发的。其中一些有名的使用者粉丝包括 MySpace, Countly, Yummly, Mozilla Persona， 以及Geekli.st。所以，如果你是一个Node开发新手的话，也许Express.js就是你应该乘坐的快速列车。

### KOA - Node.js下一代开发框架

* * *

作为一个由Express.js框架幕后开发团队进行开发和维护的另外一个Node.js开发框架，KOA是一个被热捧并冠名为Node.js的下一代开发框架的网络开发框架。因为该框架是由Express.js进化而成，所以你可以看到他们的很多相似之处，当然，区别肯定是有的了。它提供了一些额外的新功能，而该框架的中间件会把这些新功能和其他已有功能给隔离开来。另外，该框架还提供了高效开发和便于使用等功能特性来简化启动服务器和服务器相关功能的流程。

### Total.js - 一个摩登的网络应用开发Node.js框架

* * *

尽管Total.js可以被认为是一个极简型的框架，但是它依然是可以作为Node.js框架的一个补充。该框架的目标用户是那些想要打造具有非常强大的可扩展性的应用的开发者。如果你现在想要打造的是一个网络应用，而该应用也许今后会进行大量的扩展的话，Total.js也许是一个完美的选择。

### Sails.js

* * *

作为一个像Ruby On Rails一样的提供MVC开发模式模拟功能的框架，Sails.js其实是一个鲁棒的可扩展的Node.js开发框架。它自身是一个服务驱动(service-driven)的架构，而它的API集又是以数据驱动的方式进行提供的。它最大的用处应该就是用来打造多用户游戏，网络聊天，实时交互应用，以及企业泣别的Node.js应用。

# 全栈型Node.js开发框架

全栈型开发框架才是NodeJS所以发光发热的地方。大部分全栈型框架都包含了必须的应用开发基础库，完整的模版引擎，网络sockets，以及持久化的库来加速对实时可扩展的网络和移动应用进行构建。以下是当今最盛行的全栈型Node.js框架：

### Meteo - 极其简单的应用开发环境

* * *

作为一个设计成集成了所有MEAN开发框架功能的框架，Meteor是一个JavaScrtip框架的集大成者，JavaScritp既可以运行在客户端浏览器中，同时也可以在服务器端的一个Node.js容器的Meteeor服务器中运行。另外，它还支持HTML代码，CSS，以及其他有用的静态工具。 

所有这些功能在Metero框架中都是非常有弹性的组织起来的，你可以很方便的用如文件目录树请求的方式进行使用。客户端和服务端各个组件的打包和数据传送都是由Metero框架自动完成的。

### Mean.IO- 完整的MEAN栈JavaScript开发框架

* * *

MEAN.IO是一个完全的JavaScript开发框架，它是专门设计成来简化以及加速开发基于MEAN栈的网络应用的。该框架自带了可以让你把MEAN框架的四个技术进行无缝接合的工具，比如，MongoDB, Express.js, AngularJS, 以及Node.js，甚至其他开创性的如Bootstrap等技术。同时它还拥有了很多HTML和CSS以及其他额外的JavaScript代码来大大的降低你的编码时间。但是，该框架最亮眼的其实是它强悍的MVC架构。你可以使用它来创建好模块化的代码，然后用其作为工具来打造出精致的网络或移动应用。MEAN.IO包是即插即用的，所以一旦有新功能包发布，你就可以像使用npm包一样来获得并使用它们。 

MeanIO包系统把所有包都集成到mean项目里面，就好像这些代码本身就是mean自身的一部分一样。同时它也给开发者提供了所有必须的工具来把我们的包集成到我们的项目中。

－－－－－－－－－－完－－－－－－－－－－

引用英文原文：[http://www.algoworks.com/blog/most-popular-node-js-frameworks-for-app-development/](http://www.algoworks.com/blog/most-popular-node-js-frameworks-for-app-development/)

作/译者：天地会珠海分舵

微信知识共享公众号：TechGoGoGo

CSDN：[http://blog.csdn.net/zhubaitian](http://blog.csdn.net/zhubaitian)
</div>&#13;
        <script type="text/javascript"><![CDATA[
            $(function () {
                $('pre.prettyprint code').each(function () {
                    var lines = $(this).text().split('n').length;
                    var $numbering = $('<ul/>').addClass('pre-numbering').hide();
                    $(this).addClass('has-numbering').parent().append($numbering);
                    for (i = 1; i <= lines; i++) {
                        $numbering.append($('<li/>').text(i));
                    };
                    $numbering.fadeIn(1700);
                });
            });
        ]]></script></div>