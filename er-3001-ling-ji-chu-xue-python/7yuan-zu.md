**元组的特点**

* Tuple 比 list 操作速度快。如果您定义了一个值的常量集，并且唯一要用它做的是不断地

遍历它，请使用 tuple 代替 list。

* 如果对不需要修改的数据进行 “写保护”，可以使代码更安全。使用 tuple 而不是 list 如同

拥有一个隐含的 assert 语句，说明这一数据是常量。如果必须要改变这些值，则需要执

行 tuple 到 list 的转换 \(需要使用一个特殊的函数\)。

* Tuples 可以在 dictionary 中被用做 key，但是 list 不行。实际上，事情要比这更复杂。

Dictionary key 必须是不可变的。Tuple 本身是不可改变的，但是如果您有一个 list 的

tuple，那就认为是可变的了，用做 dictionary key 就是不安全的。只有字符串、整数或其

它对 dictionary 安全的 tuple 才可以用作 dictionary key。

* Tuples 可以用在字符串格式化中，后面会用到。

1.1元组

tuple是一种序列类型的数据，这点上跟list/str类似。它的特点就是其中的元素不能更改，这点

上跟list不同，倒是跟str类似；它的元素又可以是任何类型的数据，这点上跟list相同，但不同

于str。

> &gt;&gt;&gt; t = 1,"23",\[123,"abc"\],\("python","learn"\) \#元素多样性，近list
>
> &gt;&gt;&gt; t
>
> \(1, '23', \[123, 'abc'\], \('python', 'learn'\)\)
>
> &gt;&gt;&gt; t\[0\] = 8　 \#不能原地修改，近str
>
> Traceback \(most recent call last\):
>
> File "&lt;stdin&gt;", line 1, in &lt;module&gt;
>
> TypeError: 'tuple' object does not support item assignment
>
> &gt;&gt;&gt; t.append\("no"\)
>
> Traceback \(most recent call last\):
>
> File "&lt;stdin&gt;", line 1, in &lt;module&gt;
>
> AttributeError: 'tuple' object has no attribute 'append'
>
> &gt;&gt;&gt;

list如果换成tuple是否可行

> &gt;&gt;&gt; t
>
> \(1, '23', \[123, 'abc'\], \('python', 'learn'\)\)
>
> &gt;&gt;&gt; t\[2\]
>
> \[123, 'abc'\]
>
> &gt;&gt;&gt; t\[1:\]
>
> \('23', \[123, 'abc'\], \('python', 'learn'\)\)
>
> &gt;&gt;&gt; for every in t:
>
> ... print every
>
> ...
>
> 1
>
> 23
>
> \[123, 'abc'\]
>
> \('python', 'learn'\)
>
> &gt;&gt;&gt; len\(t\)
>
> 4
>
> &gt;&gt;&gt; t\[2\]\[0\] \#还能这样呀，哦对了，list中也能这样
>
> 123
>
> &gt;&gt;&gt; t\[3\]\[1\]
>
> 'learn'

所有在list中可以修改list的方法，在tuple中，都失效。

**2.元组Tuple\(\)与列表list\(\)之间的转换**

分别用list\(\)和tuple\(\)能够实现两者的转化:

> &gt;&gt;&gt; t
>
> \(1, '23', \[123, 'abc'\], \('python', 'learn'\)\)
>
> &gt;&gt;&gt; tls = list\(t\) \#tuple--&gt;list
>
> &gt;&gt;&gt; tls
>
> \[1, '23', \[123, 'abc'\], \('python', 'learn'\)\]
>
> &gt;&gt;&gt; t\_tuple = tuple\(tls\) \#list--&gt;tuple
>
> &gt;&gt;&gt; t\_tuple
>
> \(1, '23', \[123, 'abc'\], \('python', 'learn'\)\)

tuple就是一个融合了部分list和部分str属性的杂交产物

