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

> &gt;&gt;&gt; help\(set.update\)
>
> update\(...\)
>
> Update a set with the union of itself and others.
>
> &gt;&gt;&gt; s1
>
> set\(\['a', 'b'\]\)
>
> &gt;&gt;&gt; s2
>
> set\(\['github', 'qiwsir'\]\)
>
> &gt;&gt;&gt; s1.update\(s2\) \#把s2的元素并入到s1中.
>
> &gt;&gt;&gt; s1 \#s1的引用对象修改
>
> set\(\['a', 'qiwsir', 'b', 'github'\]\)
>
> &gt;&gt;&gt; s2 \#s2的未变
>
> set\(\['github', 'qiwsir'\]\)

3.删除set

> &gt;&gt;&gt; help\(set.pop\)
>
> pop\(...\)
>
> Remove and return an arbitrary set element.
>
> Raises KeyError if the set is empty.

> &gt;&gt;&gt; b\_set
>
> set\(\['\[1,2,3\]', 'h', 'o', 'n', 'p', 't', 'qiwsir', 'y'\]\)
>
> &gt;&gt;&gt; b\_set.pop\(\) \#从set中任意选一个删除,并返回该值
>
> '\[1,2,3\]'
>
> &gt;&gt;&gt; b\_set.pop\(\)
>
> 'h'
>
> &gt;&gt;&gt; b\_set.pop\(\)
>
> 'o'
>
> &gt;&gt;&gt; b\_set
>
> set\(\['n', 'p', 't', 'qiwsir', 'y'\]\)
>
> &gt;&gt;&gt; b\_set.pop\("n"\) \#如果要指定删除某个元素,报错了.
>
> Traceback \(most recent call last\):
>
> File "&lt;stdin&gt;", line 1, in &lt;module&gt;
>
> TypeError: pop\(\) takes no arguments \(1 given\)

set.pop\(\)是从set中任意选一个元素,删除并将这个值返回.但是,不能指定删除某个元素.报错信

息中就告诉我们了,pop\(\)不能有参数.此外,如果set是空的了,也报错.这条是帮助信息告诉我们

的

> &gt;&gt;&gt; help\(set.remove\)
>
> remove\(...\)
>
> Remove an element from a set; it must be a member.
>
> If the element is not a member, raise a KeyError.

set.remove\(obj\)中的obj,必须是set中的元素,否则就报错

> &gt;&gt;&gt; a\_set
>
> set\(\['i', 'a', 'qiwsir'\]\)
>
> &gt;&gt;&gt; a\_set.remove\("i"\)
>
> &gt;&gt;&gt; a\_set
>
> set\(\['a', 'qiwsir'\]\)
>
> &gt;&gt;&gt; a\_set.remove\("w"\)
>
> Traceback \(most recent call last\):
>
> File "&lt;stdin&gt;", line 1, in &lt;module&gt;
>
> KeyError: 'w'



