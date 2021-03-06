1.什么是函数？

函数是莱布尼兹在1694年开始使用，以描述曲线的一个相关量，如曲线的斜率或者曲线上的某一点。莱布尼兹所指的函数现在被称为可导函数。对于可导函数可以讨论他的极限和导数。中文的“函数”一词由清朝数学家李善兰译出。其《代数学》书中解释：“凡此变数中函（包含）彼变数者，则此为彼之函数”，也即函数指一个量随着另一个量的变化而变化，或者说一个量中包含另一个量。”（来自维基百科）

2.变量的本质——占位符

变量在本质上就是一个占位符。这是一针见血的理解。什么是占位符？就是先把那个位置用

变量占上，表示这里有一个东西，至于这个位置放什么东西，以后再说，反正先用一个符号

占着这个位置（占位符）。

3.函数实例解析

**\#!/usr/bin/env python3**

以\#开头，表示本来不在程序中运行。这句话的用途是告诉机器寻找到该设备上的

python解释器，操作系统使用它找到的解释器来运行文件中的程序代码。有的程序里写的

是/usr/bin python，表示python解释器在/usr/bin里面。但是，如果写成/usr/bin/env，则表示

零基础学Python

从if开始语句的征程 66

要通过系统搜索路径寻找python解释器。不同系统，可能解释器的位置不同，所以这种方式

能够让代码更将拥有可移植性。对了，以上是对Unix系列操作系统而言。对与windows系统，

这句话就当不存在。

**@coding:utf-8**

\#utf-8声明本 文件中代码的字符集类型是utf-8格式。初学者如果还不理解，一方

面可以去google，另外还可放一放，就先这么抄写下来，以后会讲解。

**def add\_function\(a,b\):**

\#这里是函数的开始。在声明要建立一个函数的时候，一定要使用

def（def 就是英文define的前三个字母），意思就是告知计算机，这里要声明一个函数；

add\_function是这个函数名称，取名字是有讲究的，就好比你的名字一样。在python中取

名字的讲究就是要有一定意义，能够从名字中看出这个函数是用来干什么的。从

add\_function这个名字中，是不是看出她是用来计算加法的呢？\(a,b\)这个括号里面的是这

个函数的参数，也就是函数变量。冒号，这个冒号非常非常重要，如果少了，就报错

了。冒号的意思就是下面好开始真正的函数内容了。

```py
c = a + b
#特别注意，这一行比上一行要缩进四个空格。这是python的规定，要牢记，不可
丢掉，丢了就报错。然后这句话就是将两个参数(变量)相加，结果赋值与另外一个变量
c。
print\(c\)
```

**if \_\_**_\*\*name\_\_**\_**=="\_\_mail\_\_\_":\*\*

```py
add\_function\(2,3\)
#这才是真正调用前面建立的函数，并且传入两个参数：a=2,b=3。仔细
观察传入参数的方法，就是把2放在a那个位置，3放在b那个位置（所以说，变量就是占
位符).
```

**结果：5**

声明函数的格式为：

def 函数名（参数1，参数2，参数3）：

```
函数体
```



