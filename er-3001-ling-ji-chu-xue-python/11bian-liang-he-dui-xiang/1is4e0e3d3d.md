1.

> &gt;&gt;&gt; l1
>
> \[1, 2, 3\]
>
> &gt;&gt;&gt; l2
>
> \[1, 2, 3\]
>
> &gt;&gt;&gt; l1 == l2 \#两个相等，是指内容一样
>
> True
>
> &gt;&gt;&gt; l1 is l2 \#is 是比较两个引用对象在内存中的地址是不是一样
>
> False　 \#前面的检验已经说明，这是两个东东
>
> &gt;&gt;&gt; l3 = l1　　 \#顺便看看如果这样，l3和l1应用同一个对象
>
> &gt;&gt;&gt; l3
>
> \[1, 2, 3\]
>
> &gt;&gt;&gt; l3 == l1
>
> True
>
> &gt;&gt;&gt; l3 is l1 \#is的结果是True
>
> True

is 的对比

> &gt;&gt;&gt; x = 2
>
> &gt;&gt;&gt; y = 2
>
> &gt;&gt;&gt; x is y
>
> True
>
> &gt;&gt;&gt; x = 200000
>
> &gt;&gt;&gt; y = 200000
>
> &gt;&gt;&gt; x is y \#什么道理呀，小数字的时候，就用缓存中的.
>
> False
>
> &gt;&gt;&gt; x = 'hello'
>
> &gt;&gt;&gt; y = 'hello'
>
> &gt;&gt;&gt; x is y
>
> True
>
> &gt;&gt;&gt; x = "what is you name?"
>
> &gt;&gt;&gt; y = "what is you name?"
>
> &gt;&gt;&gt; x is y \#不光小的数字，短的字符串也是
>
> False



