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

**2.1追加元素**

list.append\(\)方法

list.append\(x\)

Add an item to the end of the list; equivalent to a\[len\(a\):\] = \[x\].

即将  
新的元素x追加到list的尾部。

如：

a=\["abc",a,123\]

a.append\("def"\)

a\["abc",a,123,def"\]

equivalent  
 to a\[len\(a\):\] = \[x\]，意思是说list.append\(x\)等效于：a\[len\(a\):\]=\[x\]。这也相当于告诉我们了另外

一种追加元素的方法，并且两种方法等效。

如：

&gt;&gt;&gt; a

\['good', 'python', 'I', 'like', 100\]

&gt;&gt;&gt; a\[len\(a\):\]=\[3\] \#len\(a\),即得到list的长度，这个长度是指list中的元素个数。

&gt;&gt;&gt; a

\['good', 'python', 'I', 'like', 100, 3\]

&gt;&gt;&gt; len\(a\)

6

&gt;&gt;&gt; a\[6:\]=\['xxoo'\]

&gt;&gt;&gt; a

\['good', 'python', 'I', 'like', 100, 3, 'xxoo'\]

**2.2合并list**

list.extend\(L\)

Extend the list by appending all the items in the given list; equivalent to a\[len\(a\):\] = L.

