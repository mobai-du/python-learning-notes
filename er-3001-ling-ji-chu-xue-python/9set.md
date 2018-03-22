**1.set概括**

tuple算是list和str的杂合\(杂交的都有自己的优势,上一节的末后已经显示了\),那么set则可以堪

称是list和dict的杂合.

set拥有类似dict的特点:可以用{}花括号来定义；其中的元素没有序列,也就是是非序列类型的

数据;而且,set中的元素不可重复,这就类似dict的键.

set也有继承了一点list的特点:如可以原处修改\(事实上是一种类别的set可以原处修改,另外一种

不可以\).

理解创建set的方法:

> &gt;&gt;&gt; s1 = set\("qiwsir"\) \#把str中的字符拆解开,形成set.特别注意观察:qiwsir中有两个i
>
> &gt;&gt;&gt; s1 \#但是在s1中,只有一个i,也就是不能重复
>
> set\(\['q', 'i', 's', 'r', 'w'\]\)
>
> &gt;&gt;&gt; s2 = set\(\[123,"google","face","book","facebook","book"\]\) \#通过list创建set.不能有重复,元素可以是int/&gt;&gt;&gt; s2
>
> set\(\['facebook', 123, 'google', 'book', 'face'\]\) \#元素顺序排列不是按照指定顺序
>
> &gt;&gt;&gt; s3 = {"facebook",123} \#通过{}直接创建
>
> &gt;&gt;&gt; s3
>
> set\(\[123, 'facebook'\]\)





> &gt;&gt;&gt; s3 = {"facebook",\[1,2,'a'\],{"name":"python","lang":"english"},123}
>
> Traceback \(most recent call last\):
>
> File "&lt;stdin&gt;", line 1, in &lt;module&gt;
>
> TypeError: unhashable type: 'dict'
>
> &gt;&gt;&gt; s3 = {"facebook",\[1,2\],123}
>
> Traceback \(most recent call last\):
>
> File "&lt;stdin&gt;", line 1, in &lt;module&gt;
>
> TypeError: unhashable type: 'list'

从上述实验中,可以看出,通过{}无法创建含有list/dict元素的set.



> &gt;&gt;&gt; s1
>
> set\(\['q', 'i', 's', 'r', 'w'\]\)
>
> &gt;&gt;&gt; s1\[1\] = "I"
>
> Traceback \(most recent call last\):
>
> File "&lt;stdin&gt;", line 1, in &lt;module&gt;
>
> TypeError: 'set' object does not support item assignment
>
> &gt;&gt;&gt; s1
>
> set\(\['q', 'i', 's', 'r', 'w'\]\)
>
> &gt;&gt;&gt; lst = list\(s1\)
>
> &gt;&gt;&gt; lst
>
> \['q', 'i', 's', 'r', 'w'\]
>
> &gt;&gt;&gt; lst\[1\] = "I"
>
> &gt;&gt;&gt; lst
>
> \['q', 'I', 's', 'r', 'w'\]

上面的探索中,将set和list做了一个对比,虽然说两者都能够做原处修改,但是,通过索引编号\(偏

移量\)的方式,直接修改,list允许,但是set报错.

