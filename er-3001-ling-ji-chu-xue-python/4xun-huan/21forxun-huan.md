1.简例

如果要让打印的在一行，可以用下面的方法，在打印的后面加一个逗号（英文）

> &gt;&gt;&gt; for i in hello:
>
> ... print i,
>
> ...
>
> w o r l d
>
> &gt;&gt;&gt; for i in hello:
>
> ... print i+",", \#为了美观，可以在每个字符后面加一个逗号分割
>
> ...
>
> w, o, r, l, d,
>
> &gt;&gt;&gt;

偏移量

> &gt;&gt;&gt; for i in range\(len\(hello\)\):
>
> ... print hello\[i\]
>
> ...
>
> w
>
> o
>
> r
>
> l
>
> d

其工作方式是：

1. len\(hello\)得到hello引用的字符串的长度，为5

2. range\(len\(hello\),就是range\(5\),也就是\[0, 1, 2, 3, 4\],对应这"world"每个字母的编号，即偏

移量。

1. for i in range\(len\(hello\)\),就相当于for i in \[0,1,2,3,4\],让i依次等于list中的各个值。当i=0

时，打印hello\[0\]，也就是第一个字符。然后顺序循环下去，直到最后一个i=4为止。

案例：

找出100以内的能够被3整除的正整数

> \#! /usr/bin/env python
>
> \#coding:utf-8
>
> a = \[\]
>
> for n in range\(1,100\):
>
> if n%3 == 0:
>
> a.append\(n\)
>
> print \(a\)

代码运行结果：

> \[3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36, 39, 42, 45, 48, 51, 54, 57, 60, 63, 66, 69, 72,



