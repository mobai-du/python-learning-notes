**1.dict的特点**

dict是可变的

dict可以存储任意数量的Python对象

dict可以存储任何python数据类型

dict以：key:value，即“键：值”对的形式存储数据，每个键是唯一的。

dict也被称为关联数组或哈希表。

> &gt;&gt;&gt; person = {"name":"qiwsir","site":"qiwsir.github.io","language":"python"}
>
> &gt;&gt;&gt; person
>
> {'name': 'qiwsir', 'language': 'python', 'site': 'qiwsir.github.io'}

"name":"qiwsir"就是一个键值对，前面的name叫做键（key），后面的qiwsir是前面的键所对

应的值\(value\)。在一个dict中，键是唯一的，不能重复；值则是对应于键，值可以重复。键值

之间用\(:\)英文的分号，每一对键值之间用英文的逗号\(,\)隔开。

如下，演示了从一个空的dict开始增加内容的过程：

> &gt;&gt;&gt; mydict = {}
>
> &gt;&gt;&gt; mydict
>
> {}
>
> &gt;&gt;&gt; mydict\["site"\] = "qiwsir.github.io"
>
> &gt;&gt;&gt; mydict\[1\] = 80
>
> &gt;&gt;&gt; mydict\[2\] = "python"
>
> &gt;&gt;&gt; mydict\["name"\] = \["zhangsan","lisi","wangwu"\]
>
> &gt;&gt;&gt; mydict
>
> {1: 80, 2: 'python', 'site': 'qiwsir.github.io', 'name': \['zhangsan', 'lisi', 'wangwu'\]}
>
> &gt;&gt;&gt; mydict\[1\] = 90 \#如果这样，则是修改这个键的值
>
> &gt;&gt;&gt; mydict
>
> {1: 90, 2: 'python', 'site': 'qiwsir.github.io', 'name': \['zhangsan', 'lisi', 'wangwu'\]}

方法2:

> &gt;&gt;&gt; name = \(\["first","Google"\],\["second","Yahoo"\]\) \#这是另外一种数据类型，称之为元组，后面会讲到
>
> &gt;&gt;&gt; website = dict\(name\)
>
> &gt;&gt;&gt; website
>
> {'second': 'Yahoo', 'first': 'Google'}

方法3:

这个方法，跟上面的不同在于使用fromkeys

> &gt;&gt;&gt; website = {}.fromkeys\(\("third","forth"\),"facebook"\)
>
> &gt;&gt;&gt; website
>
> {'forth': 'facebook', 'third': 'facebook'}

需要提醒的是，这种方法是从新建立一个dict。

