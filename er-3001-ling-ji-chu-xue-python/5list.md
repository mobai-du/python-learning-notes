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

> &gt;&gt;&gt; a

\['good', 'python', 'I', 'like', 100, 3\]

&gt;&gt;&gt; len\(a\)

6

&gt;&gt;&gt; a\[6:\]=\['xxoo'\]

&gt;&gt;&gt; a

\['good', 'python', 'I', 'like', 100, 3, 'xxoo'\]

**2.2合并list**

list.extend\(L\)

Extend the list by appending all the items in the given list; equivalent to a\[len\(a\):\] = L.

通过将所有元素追加到已知list来扩充它，相当于a\[len\(a\)\]= L

&gt;&gt;&gt; la

\[1, 2, 3\]

&gt;&gt;&gt; lb

\['qiwsir', 'python'\]

&gt;&gt;&gt; la.extend\(lb\)

&gt;&gt;&gt; la

\[1, 2, 3, 'qiwsir', 'python'\]

&gt;&gt;&gt; lb

\['qiwsir', 'python'\]

上面的例子，显示了如何将两个list，一个是la，另外一个lb，将lb追加到la的后面，也就是把

lb中的所有元素加入到la中，即让la扩容。

区别：append是整建制地追加，extend是个体化扩编。

**3.list中某元素出现的个数**

list.count\(x\)

Return the number of times x appears in the list.

统计元素中出现的个数

&gt;&gt;&gt; la = \[1,2,1,1,3\]

&gt;&gt;&gt; la.count\(1\)

**4.list元素中的位置**

list.index\(x\)，x是list中的一个元素，这样就能够检索到该元素在list中的位置了。这才是真正

的索引，注意那个英文单词index。

