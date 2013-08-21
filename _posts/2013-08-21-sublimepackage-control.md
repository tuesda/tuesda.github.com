---
layout: post
title: "sublime安装package control"
description: ""
category: 
tags: []
---
{% include JB/setup %}


* 用`` ctrl + ` ``打开console

* 将以下代码粘贴进去  
>`import urllib2,os;pf='Package Control.sublime-package';`  
>`ipp=sublime.installed_packages_path();`  
>`os.makedirs(ipp) if not os.path.exists(ipp) else None;`  
>`open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read())`

* 重启Sublime，如果在 Preferences -> Package Settings中见到Package Control这一项，就说明安装成功了。