title: XCode调试的那些事儿（一）
date: 2015-10-10 11:09:39
categories: iDev
tags: [Xcode,调试]
---
苹果基本上每年都会有一次大的系统升级，开发工具当然更需要提前一步。不过每次的更新换代，或多或少会带来很多诡异的问题。
我的项目原先是在Xcode6.4上的，很顺利的升级到了7.0，编译运行都很正常。
可是总是会在固定的代码位置自动停下来，和下了断点的效果是一样一样的。提示：Thread 1: breakpoint 3.1
情景重现：
![断点](https://raw.githubusercontent.com/idealife/idealife.github.io/master/img/2-0.png)
难道是代码有异常？注释掉这回代码就正常了，但是@try @catch并没有捕获任何异常。
真的是奇了怪了。
整个项目clean后问题依旧，然后各种捣鼓……
搜了一圈有人指出是更新开发环境引起的症状，[%>_<%]，废了半天时间找代码问题，最后竟然是苹果的事情。
<!--more-->
屏蔽的方法是在调试窗口中，把全局的断点状态标记关闭后，就能顺利执行代码了。
![方法](https://raw.githubusercontent.com/idealife/idealife.github.io/master/img/2-1.png)
吐槽：苹果，请你好好用心做产品吧，现在黑iCloud的人也越来越多了！

