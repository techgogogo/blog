title: 谢绝艳照门 - 手把手教你把当今最hit的家庭监控IP Camera变得网络安全起来
tags:
  - Linux
  - OpenVPN
  - 加密
  - 监控技术
  - 网络安全
id: 530
categories:
  - Hacker News
date: 2015-02-11 14:23:00
---

<div id="article_content" class="article_content">&#13;

![](http://img.blog.csdn.net/20150210213554253?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<span style="color: rgb(51, 102, 255);">IP Camerars现在已经越来越便宜了，很多人都可以买得起，并且大家也乐意去购买，因为它们的确是用来监控你在高房价的中国购买的爱巢的非常便利的设备。当然，配套的监控应用也层出不穷，从通用的家庭安全监控到北鼻监护，宠物监护等等等不一而足。大部分这些cameras都基本上具有内建的网络服务器和API接口来让大家可以从任何只要有网络接入的地方来通过网络浏览器或者你的爱phone来进行访问。当然了，这种情况下你是必须在你的路由器上设置端口转发才能实现的了(</span><span style="color: rgb(255, 102, 102);">天地会珠海分舵注：如果你是个妹纸的话，那你是时候敲响隔壁老王的门了</span><span style="color: rgb(51, 102, 255);">)。</span>

<span style="color: rgb(51, 102, 255);">监控技术哪家强？相信你不再会去找南翔。那么问题来了，连接访问这些IP Cameras的大部分公共连接接入其实都是没有对数据进行加密的，且所谓的安全仅限于用户名和密码的验证而已。也许有些地方还是增强了一些如防止暴力破解的保护功能，但是，把你购买的最新的最潮的IP Camera的网络连接直接暴露到公共网络外面，难道你真的想学陈冠希老师来通过艳照门做一回八卦新闻网站和周刊的头条霸主吗？相信这不是大家想要的吧？毕竟，连玛莲梦露在风吹起来的时候都会下意识的捂着裙子，连苍老师都要从良了，你该不会是想要“不小心”把你的床上英雄史在网上分30集不停的循环播放再播放的。</span>

![](http://img.blog.csdn.net/20150210220110731?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

# <span style="font-size: 18px; color: rgb(51, 102, 255);">通过VPN进行访问</span>

<span style="color: rgb(51, 102, 255);">众多方法之一就是避免在你家的路由中做端口转发到你的IP Camera的设置，而是通过VPN来进行穿透直接通过公共网络访问你的IP Camera。如果你是使用vpn访问你的家庭网络的话，你就在等用于本地网络安全的情况下对你的IP Camera进行安全访问了。也就是你的反问设备和你的IP Camerar之间的通信数据是被加密了的。</span>

<span style="color: rgb(51, 102, 255);">那么今天哥就来跟你说说应该如何已最简单的方式在你的家庭网络环境中安装OpenVPN，当然，一如既往，在你根据哥的知道安装好后，可别忘了针对网络安全方面做更多的研究，然后如果你发现或者学习到了任何有意思的东东的话，切记要在我们网站的评论区给出你的领悟哦。</span>

![](http://img.blog.csdn.net/20150210221139397?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

# <span style="font-size: 18px; color: rgb(51, 102, 255);">安装OpenVPN</span>

<span style="color: rgb(51, 102, 255);">以哥斥巨资购买的长宽3米的珠江大桥第四个桥孔的爱巢的网络环境为例，哥现在爱巢里用的可是Linux发行版炙手可热的Ubuntu 14服务器版本兼且是64位的炒作系统哦，噢，sorry，是操作系统，没炒作。因此呢，好吧，那么我们的安装流程就基于它吧。哥这里就先假设其他的linux发行版都是类似的了(天地会珠海分舵注: 当然，你非要拿哥minix教学系统跟我较劲的话我也没有办法，虽然想当年哥对该操作系统可是有透彻的源码研究和分析的，但可惜“当年”这个词在这里需要用“10年”来代理)。对了，大家转发哥的博客的时候记得加上个引用出处呗，我这里做个榜样和模版，“本文往下的一些步骤是引用了OpenVPN官网内容的，我爱OpenVPN, OpneVPN是最好的，OpenVPN是无私奉献的，我要给OpenVPN捐助1万美刀..."，大家有引用哥的文章的话就按照这种格式去填写就好了， 只是别忘了把里面的"OpenVPN"改成"天地回珠海分舵" ；如果是妹纸的话也可以在以上基础上把 “一万美刀“改成“我自己”，不捐助就算了。哥也不是个见钱眼开的人，只是不见钱就眼睛瞪的老大如张飞罢了。</span>

![](http://img.blog.csdn.net/20150210223337459?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## <span style="color: rgb(51, 102, 255);">下载安装OpenVPN</span>

<span style="color: rgb(51, 102, 255);">那么我们要做的第一步就是去下载正确的OpenVPN安装包，你可以从[这里](https://openvpn.net/index.php/access-server/download-openvpn-as-sw.html)找到它。</span>

<span style="color: rgb(51, 102, 255);">那么就去下载吧。下载完成后请打开你的终端并定位到该安装包所下载存放的位置，假如你是下载到~/Downloads的话，就请定位到该目录下面。然后就执行dpkg命令来安装该安装包。</span>

![](http://img.blog.csdn.net/20150210223829273?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<span style="color: rgb(51, 102, 255);">执行了以上命令后，你大致会看到如下的输出信息：</span>

![](http://img.blog.csdn.net/20150210224059283?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![](http://img.blog.csdn.net/20150210224221664?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<span style="color: rgb(51, 102, 255);">基本上来说，该安装包会包所有包括你的认证都会安装好，因为我们一直的目标都是简单即是美。在安装好后请记住你的管理平台地址，因为你将会用到它的。如果你真的没有记住的话，那么尝试下用例如https://192.168.0.9:943/admin“这个地址尽心访问吧，注意前面的ip要换成你自己机器的ip地址了，因为一般我们的默认地址都是这么设置的。</span>

<span style="color: rgb(51, 102, 255);">还有就是我们的默认用户是openvpn。这里有一点很重要的是，openvpn这个用户是根服务器用户绑定的，当初始化安装完成之后，该初始化脚本同时会创建一个openvpn的用户来给你的Ubuntu服务器使用。下一步需要做的事情就是给你的openvpn这个用户添加一个强口令了，这里敬请你使用随机密码生成器来生成如1Password之类的数字和大小写都有的口令来保证你在一开始就拥有一个不容易攻破的密码。</span>

<span style="color: rgb(51, 102, 255);">如上所提及的，改变密码的命令如下：</span>

![](http://img.blog.csdn.net/20150210233051228?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![](http://img.blog.csdn.net/20150210233206966?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## <span style="color: rgb(51, 102, 255);">创建另外一个用户</span>

<span style="color: rgb(51, 102, 255);">下一步需要做的事情就是去创建另外一个用户以便我们今后用来接管掌控默认用户openvpn的管理权限。这其实也是也是我常用的安全保障手段之一，为了以防万一，在特定情况下使用另外一个用户来取代一个默认的用户。</span>

<span style="color: rgb(51, 102, 255);">故此，请选取一个唯一的用户名来创建你的用户。在创建好后直接使用一个高强度的安全密码。在我们的教程中我们使用的是用户padawan。我们在下一个小节依然会用到。</span>

![](http://img.blog.csdn.net/20150210233852111?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![](http://img.blog.csdn.net/20150210233949616?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## <span style="color: rgb(51, 102, 255);">指派新的管理员</span>

<span style="color: rgb(51, 102, 255);">原文再接上一回，请通过浏览器登录你的OpenVPN管理平台界面。在提醒一次，这应该是如https://192.168.0.9:943/admin这样的url格式。登录过程请使用上面你说设置的openvpn用户和对应的密码。</span>

<span style="color: rgb(51, 102, 255);">当登录成功后你将会看到状态概览页面，该页面会为你展示服务器版本，端口等等信息。</span>

<span style="color: rgb(51, 102, 255);">在左边的导航栏中请导航到"用户权限"位置。当该页面加载完成后，请在该页面增加一个如下所示的padawan的用户。</span>

![](http://img.blog.csdn.net/20150210235715488?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![](http://img.blog.csdn.net/20150210235929805?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

<span style="color: rgb(51, 102, 255);">点击保存设置并根据以下步骤进行设置：</span>

1.  <span style="color: rgb(51, 102, 255);">保存后，正常来说opevpn服务器应该自动进行服务重启的，但是上一次我却必须要手动重启才能激活用户。</span>
2.  <span style="color: rgb(51, 102, 255);">你可以通过后来命令如下来重启OpenVPN: sudo service openvpnas restart</span>
3.  <span style="color: rgb(51, 102, 255);">回到用户权限页面</span>
4.  <span style="color: rgb(51, 102, 255);">为你新创建的用户padawan勾选"Admin"权限选项</span>
5.  <span style="color: rgb(51, 102, 255);">登出管理平台</span>
6.  <span style="color: rgb(51, 102, 255);">使用padawan用户来重新登录。这一步是用来测试该用户是否正常设置好。</span>
7.  <span style="color: rgb(51, 102, 255);">回到用户权限界面</span>
8.  <span style="color: rgb(51, 102, 255);">启动openvpn的拒绝访问权限。当有了新的管理权限用户padawan后，我们再也不需要该默认用户了。</span><div style="color: rgb(68, 68, 68); font-family: 'Century Schoolbook', Georgia, Times, serif; font-size: 10pt; line-height: 18px;">![](http://img.blog.csdn.net/20150211000745072?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
</div>

## <span style="color: rgb(51, 102, 255);">开启谷歌身份认证器</span>
<div style="font-family: 'Century Schoolbook', Georgia, Times, serif; font-size: 10pt; line-height: 18px;"><span style="color: rgb(51, 102, 255);">为了安全起见，我们会增加多一层的安全验证，我们希望启用的是谷歌身份安全认证器。在过去的版本中我们必须把该认证器一步步建立起来，但是在本版本的OpenVPN中就简单多了：</span></div><div>

1.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">导航到"客户设置"页面</span></span>
2.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">勾选"需要用户每次登录时提供谷歌身份认证器提供的一次性密码"</span></span>
3.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">保存设置</span></span><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">恭喜，你现在已经有个谷歌认证器的支持了。往下你需要做的就是去建立你的认证器应用而已了。我自己使用的时iOS版本的谷歌认证器，但我相信安卓版本的的设置过程应该时一致如下所示的：</span></span></div></div><div>

1.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">在你的网络浏览器中打开你的vpn服务器</span></span>
2.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">老调重弹，改地址应该时如下所示格式的：https://192.168.0.9。请注意使用的时https且该地址不会带有任何端口相关信息。</span></span>
3.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">过程中将会有一个弹出框提示你要下载OpenVPN的连接客户端，先不用管它，我们可以在今后来安装</span></span>
4.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">往下翻页后你会看到一个二维码以及一个唯一的代码，你可以把该码输入到谷歌身份认证器里面</span></span>
5.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">拷贝并粘贴该唯一的代码</span></span>
6.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">打开你的谷歌身份验证器并把该新号码输入进去</span></span><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">再次恭喜，谷歌身份验证器已经在你的不懈努力下建立好了。‘</span></span></div></div><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(68, 68, 68);"><span style="font-size: 13.3333339691162px; line-height: 18px;">![](http://img.blog.csdn.net/20150211002413848?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
</span></span></div>

## <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="line-height: 18px;">开启VPN的网络访问权限</span></span>
<div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">既然我们已经把基本安全配置给搞定了，那么下一步我们就应该需要去把该VPN服务器建立起来给公共网络进行访问了。</span></span></div><div>

1.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">登录OpenVPN网络管理平台</span></span>
2.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">选择"服务器网络设置"</span></span>
3.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">在"主机名称或IP地址"中输入你的公开IP地址</span></span>
4.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">暂时先把其他设置保持不变</span></span>
5.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">保存设置</span></span><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">下一步就是去对你的家庭路由进行OpenVPN端口的转发了。鉴于每个提供商的路由都有不同的设置界面，所以我这里不能不能详细的告诉你该如何在你的路由中进行设置。但是总的来说，你需要做的事情就就是把你在“服务器网络设置”页面看到的TCP和UDP端口进行转发，默认来说这些端口会是443和1194。</span></span></div></div><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(68, 68, 68);"><span style="font-size: 13.3333339691162px; line-height: 18px;">![](http://img.blog.csdn.net/20150211003509767?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
</span></span></div>

## <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="line-height: 18px;">建立VNP客户端</span></span>
<div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">其实这一小节还真的没有多少东西好说的，你要做的事情首先就是从AppStore中下载OpenVPN的客户端并安装好。</span></span></div><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">在此过程中当提示添加一个档案的时候，只需要选择“从OpenVPN访问服务器倒入档案"就好了。在该页面提供的输入框中，请输入你的公共IP地址。然后该过程就会自动下载对应的正确的档案，然后你所需要做的事情就是在你的OpenVPN连接应用中点击打开功能而已。</span></span></div><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">完成以上步骤后，你的档案应该已经建立起来且你已经能通过你的用户名和密码登录到你的VPN了。因为我们前面启动了谷歌身份认证器，你还需要输入你的认证器令牌。</span></span></div><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">为了保证你在你的电脑上安装了正确的VPN软件，请跟随以下步骤：</span></span></div><div>

1.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">登录你的VPN客户端地址，也就是以https开始的IP地址</span></span>
2.  <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">点击下载客户端。在我的Mac机器上，在客户端安装完成后，档案已经自动建立好了。所有我需要做的事情仅仅是使用正确的身份凭证来进行登录而已。</span></span><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(68, 68, 68);"><span style="font-size: 13.3333339691162px; line-height: 18px;">![](http://img.blog.csdn.net/20150211005039609?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
</span></span></div></div>

## <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="line-height: 18px;">访问你的IP Camera</span></span>
<div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">这个是本教程最容易的一部分了，你首先需要做的仅仅是保证你的VPN连接是ok的。然后你就既可以通过网络浏览器或便携式的iOS软件如IP Cam Lite(个人看来这款工具是便宜且实用的)来访问你的IP Camerar了，我相信Android同样也有类似的应用供你选择。</span></span></div><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">无论你用的是哪种访问方式，到了现在，相信你已经可以通过本地地址加上正确的端口地址来访问你的IP Camera了。</span></span></div><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(68, 68, 68);"><span style="font-size: 13.3333339691162px; line-height: 18px;">
</span></span></div><div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(68, 68, 68);"><span style="font-size: 13.3333339691162px; line-height: 18px;">![](http://img.blog.csdn.net/20150211005640498?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvemh1YmFpdGlhbg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
</span></span></div>

## <span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="line-height: 18px;">闭幕</span></span>
<div><span style="font-family: 'Century Schoolbook', Georgia, Times, serif; color: rgb(51, 102, 255);"><span style="font-size: 13.3333339691162px; line-height: 18px;">恭喜恭喜，通过你的VPN服务器对你的IP Camera进行简易访问的教程就到此为止了。如我们之前所言，这可能是一个最简单的安装教程了，当然，如果要把安全性做的更好的话，你尚需要做很多其他的事情。我希望本文能帮助到你并期望如果你有更进一步的想法和问题的话，可以在评论中给我们留下只言片语。谢谢。</span></span></div><div>
</div><div><table border="1" cellspacing="0" cellpadding="0" style="color: rgb(54, 46, 43); font-family: Arial; font-size: 14px; line-height: 26px;"><tbody><tr><td valign="top" style="background: rgb(250, 191, 143);">

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
</div></div>