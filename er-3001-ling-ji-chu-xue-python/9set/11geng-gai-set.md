1.1查看set内置函数

dir\(set\)

help\(set\)

> &gt;&gt;&gt; a\_set = {'a','i'} \#这回就是set了吧
>
> &gt;&gt;&gt; type\(a\_set\)
>
> &lt;type 'set'&gt; \#果然
>
> &gt;&gt;&gt; a\_set.add\("qiwsir"\) \#增加一个元素
>
> &gt;&gt;&gt; a\_set \#原处修改,即原来的a\_set引用对象已经改变
>
> set\(\['i', 'a', 'qiwsir'\]\)
>
> &gt;&gt;&gt; b\_set = set\("python"\)
>
> &gt;&gt;&gt; type\(b\_set\)
>
> &lt;type 'set'&gt;
>
> &gt;&gt;&gt; b\_set
>
> set\(\['h', 'o', 'n', 'p', 't', 'y'\]\)
>
> &gt;&gt;&gt; b\_set.add\("qiwsir"\)
>
> &gt;&gt;&gt; b\_set
>
> set\(\['h', 'o', 'n', 'p', 't', 'qiwsir', 'y'\]\)
>
> &gt;&gt;&gt; b\_set.add\(\[1,2,3\]\) \#这样做是不行滴,跟前面一样,报错.
>
> Traceback \(most recent call last\):
>
> File "&lt;stdin&gt;", line 1, in &lt;module&gt;
>
> TypeError: unhashable type: 'list'
>
> &gt;&gt;&gt; b\_set.add\('\[1,2,3\]'\) \#可以这样!
>
> &gt;&gt;&gt; b\_set
>
> set\(\['\[1,2,3\]', 'h', 'o', 'n', 'p', 't', 'qiwsir', 'y'\]\)

**2.合并set**

set.update\(s2\)

