一、查看Python的版本

python -v

二、新建Python文件

eg:\#!/usr/bin/env python3\#

\(脚本语言的第一行，目的就是指出，你想要你的这个文件中的代码用什么可执行程序去运行它，就这么简单。\#!/usr/bin/env python这种用法是为了防止操作系统用户没有将python装在默认的/usr/bin路径里。当系统看到这一行的时候，首先会到env设置里查找python的安装路径，再调用对应路径下的解释器程序完成操作。\)

print\("hello,world"\);

运行：python3 hello.py

