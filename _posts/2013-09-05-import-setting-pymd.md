---
layout: post
title: "import settings py.md"
description: "Import settings in django"
category: django
tags: [django,path,settings]
---
{% include JB/setup %}

ImageField类里面存放的是图片的相对地址，不过我用PIL库来处理图片，打开的时候ImageField的相对地址能打开图片，但不知道为什么保存的时候用ImageField中的相对地址不行。只得想办法得到绝对地址，绝对地址是settings.py中MEDIA_ROOT+ImageField的相对地址，但不知道如何引入settings.py中的MEDIA_ROOT变量。最后找到了，

	form django.conf import settings

然后通过`settings.MEDIA_ROOT`就可得到MEDIA_ROOT中的值。
关于我上面的问题，肯定有其他比较简单的方法解决，我不过暂时不知道，只能用这个笨办法了，希望后面可以找到好的办法解决
