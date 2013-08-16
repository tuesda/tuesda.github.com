---
layout: post
title: "win7下用goagent翻墙教程"
description: "goagent功能比较强大"
category: 网络
tags: [goagent,翻墙,chrome,AGE,win7,]
tagline: 手把手教你如何翻墙
---
{% include JB/setup %}

 


<img class="cat-teacher" src="http://13q.imghost.us/M0/23e0af95f42bbb18be9de0189346034d.jpeg" />

Github的头像是那只猫，要想在Github上有自定义的猫，就需要在[Gravatar](http://en.gravatar.com)上注册自己的头像，Github会根据邮件地址去获取相应的头像。

但是发现在Gravatar上注册一个账号需要<http://wordexpress.com/>的账号，但是<http://wordexpress.com/>被墙掉了，没办法上。所以我就想找个梯子，随手google了一下。在百度经验发现了一个帖子：[如何用chrome翻墙上网](http://jingyan.baidu.com/article/08b6a591eaccd614a9092243.html)，感觉挺正规的，就跟着试了试，虽然过程比较坎坷，但最终还是成功了，还是挺兴奋的。

我实验的过程中发现了这么几个问题：

* 在我试的过程中，发现那个百度经验的教程中还有点不足，这里有一个视频[goagent](http://v.youku.com/v_show/id_XNTM5ODI0Nzg0.html)，也是讲**goagent**的。里面比较有用的就是最后介绍chrome插件Proxy SwitchySharp的基本选项里关于直接连接、goagent、自动转换的区别。

* 在所有的事情都按照教程做完之后发现只有<http://www.youtube.com/>显示正常。<http://www.facebook.com/>和<http://twitter.com/>都不能正常显示，显示说证书有问题，我就在网上搜了解决方案，发现了两个帖子比较好：<http://www.yooloo.com/thread-3274-1-1.html>和<http://blog.netsh.org/posts/goagent-https-ssl-error_1013.netsh.html>。按照这两个帖子做完之后发现一切都正常了，不是网速什么的原因。**注意：配置完之后要记得重启浏览器！**

* 出现的问题都解决后，我就准备去<http://wordexpress.com/>注册，结果显示不能注册。google后有人说是被墙掉了，顿时悲从中来。。。。还好苍天有眼，让我看见了这篇日志：<http://yhzhtk.info/2013/06/14/1-sign-up-wordpress.html/>。其中的重点就是，通过goagent上网不能在<http://wordexpress.com/>注册，但是可以通过`zi_you_men`注册。

几个比较好的，要学习的网站：  

> [appengine.google.com](https://appengine.google.com/)  
> [goagent主页](https://code.google.com/p/goagent/)  
> [最为详细的的goagent教程](https://code.google.com/p/goagent/wiki/InstallGuide)