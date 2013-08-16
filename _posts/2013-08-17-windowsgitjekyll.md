---
layout: post
title: "windows下安装git客户端和jekyll"
description: "git and jekyll"
category: git&github
tags: [github,win7,git,github,jekyll,]
tagline: how to get start about github
---
{% include JB/setup %}



###Windows下安装git客户端及配置

[windows下面安装git客户端以及配置](https://help.github.com/articles/set-up-git)git安装比较简单，只要按照链接里面的方法一步一步来就好了。

###在Windows系统配置Jekyll

[Jekyll](http://jekyllrb.com/)是一个简单的网站静态页面生成工具。由于使用Ruby编写的，所以要先安装ruby。

具体过程如下：

1.	安装Ruby：在Windows系统上使用rubyinstaller，[点我下载](http://rubyinstaller.org/downloads/)(笔者用的是Ruby 2.0.0-p247）。安装到某个磁盘，比如D:\Ruby200，在安装界面把所有的选项都选上。
2. 	安装Ruby DevKit：[点我下载](https://github.com/downloads/oneclick/rubyinstaller/DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe) 把下载下来的DevKit解压到某个磁盘例如D:\devkit。在该目录运行如下命令：

		ruby dk.rb init
	生成了一个config.xml配置文件，里面包含Ruby200的安装目录（D:\Ruby200）然后运行如下命令

		ruby dk.rb install
3. 	然后运行如下命令安装jekyll:

		gem install jekyll
	这里有个问题，就是gem的安装文件默认地址是<https://rubygems.org/>。但是这个地址网速太慢，要换成<http://ruby.taobao.org/>.查看镜像地址的命令是：

		gem source -l
	删除<https://rubygems.org/>的命令是：

		gem source -r https://rubygems.org/
	添加淘宝镜像地址<http://ruby.taobao.org/>的命令是：

		gem source -a http://ruby.taobao.org/
	最后在用`gem source -l`命令确认一下。然后安装jekyll。最后在安装一下rdiscount：

		gem install rdiscount

**注意：windows下jekyll本地生成的页面可能会出现中文乱码解决方法如下：**

如果博文文件有 utf-8 编码的，需要打开 Ruby 安装目录下的 lib\ruby\gems\1.9.1\gems\jekyll-0.11.2\lib\jekyll\convertible.rb 文件（找不到可以搜索，版本号可能会有不同），把

		self.content = File.read(File.join(base, name))
替换成

		self.content = File.read(File.join(base, name), :encoding => "utf-8")
保证后续操作不会因编码问题影响生成本地网站。如果文件中包含中文，一定要使用UTF8格式，否则本地生成会失效
