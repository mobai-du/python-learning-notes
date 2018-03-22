**1.list索引**

&gt;&gt;&gt; a\[:2\] \#跟str中的类似，切片的范围是：包含开始位置，到结束位置之前

\['2', 3\] \#不包含结束位置

&gt;&gt;&gt; a\[1:\]

\[3, 'qiwsir.github.io'\]

&gt;&gt;&gt; a\[-1\] \#负数编号从右边开始

'qiwsir.github.io'

&gt;&gt;&gt; a\[-2\]

3

&gt;&gt;&gt; a\[:\]

\['2', 3, 'qiwsir.github.io'\]

**2.对list的操作**

2.1追加元素

list.append\(\)方法

list.append\(x\)

Add an item to the end of the list; equivalent to a\[len\(a\):\] = \[x\].

即将  
新的元素x追加到list的尾部。

如：

a=\["abc",a,123\]

a.append\("def"\)

a\["abc",a,123,def"\]

