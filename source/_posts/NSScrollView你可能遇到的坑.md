title: NSScrollView你可能遇到的坑
date: 2015-10-21 23:13:56
categories: iDev
tags: [Xcode, Mac OS X]
---
换了一台用来开发的Mac【就叫Mac A吧】，程序运行一切正常。
可是仔细一看，发现程序中某个界面的表格区域竟然默认显示了滚动条，很是奇怪。
![图片](https://raw.githubusercontent.com/idealife/idealife.github.io/master/img/4_2.png)
因为我明明设置NSScrollView的属性是Automatically Hide Scroller，如图。正常情况下我鼠标放到表格区域才会出现滚动条的。
![图片](https://raw.githubusercontent.com/idealife/idealife.github.io/master/img/4_1.png)
又特地去原来的Mac【Mac B】上查看效果，滚动条默认是不显示的，两个都是10.9.5的系统，显示效果竟然不一样，有点想不明白。随后又找了个10.10的系统【Mac C】对比效果，也是不会自动显示滚动条的。正当一筹莫展中，猛然发现Mac A的Xcode也是默认显示着滚动条。
难道是系统的某个显示效果设置引起的？
<!--more-->
费尽周折，果不其然，在“偏好设置”–“通用”中找到了滚动条的显示设置，如下图
![图片](https://raw.githubusercontent.com/idealife/idealife.github.io/master/img/4_3.png)