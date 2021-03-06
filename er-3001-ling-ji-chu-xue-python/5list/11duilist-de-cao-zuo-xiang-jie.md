**1.1向list中插入一个元素**

这种改变的含义只它的大小即所容纳元素的  
个数以及元素内容，可以随时直接修改，而不用进行转换。这和str有着很大的不同。对于  
str，就不能进行字符的追加。请看官要注意比较，这也是str和list的重要区别。  
与list.append\(x\)类似，list.insert\(i,x\)也是对list元素的增加。只不过是可以在任何位置增加一个  
元素。

> &gt;&gt;&gt; all\_users
>
> \['qiwsir', 'github', 'io'\]
>
> &gt;&gt;&gt; all\_users.insert\("python"\) \#list.insert\(i,x\),要求有两个参数，少了就报错
>
> Traceback \(most recent call last\):
>
> File "&lt;stdin&gt;", line 1, in &lt;module&gt;
>
> TypeError: insert\(\) takes exactly 2 arguments \(1 given\)
>
> &gt;&gt;&gt; all\_users.insert\(0,"python"\)
>
> &gt;&gt;&gt; all\_users
>
> \['python', 'qiwsir', 'github', 'io'\]
>
> &gt;&gt;&gt; all\_users.insert\(1,
>
> &gt;&gt;&gt; all\_users
>
> \['python', 'http://', 'qiwsir', 'github', 'io'\]
>
> &gt;&gt;&gt; length = len\(all\_users\)
>
> &gt;&gt;&gt; length
>
> 5
>
> &gt;&gt;&gt; all\_users.insert\(length,"algorithm"\)
>
> &gt;&gt;&gt; all\_users
>
> \['python', 'http://', 'qiwsir', 'github', 'io', 'algorithm'\]

list.insert\(i,x\),将新的元素x 插入到原list中的list\[i\]前面

如果i==len\(list\)，意思是在后面追加，就等同于list.append\(x\)

**1.2删除list中的元素**

list.remove\(x\)

Remove the first item from the list whose value is x. It is an error if there is no such

item.

> a=\["abc",123,8\]
>
> a.remove\(8\)
>
> a\["abc",123\]

list.pop\(\[i\]\)

Remove the item at the given position in the list, and return it. If no index is

specified, a.pop\(\) removes and returns the last item in the list. \(The square

brackets around the i in the method signature denote that the parameter is

optional, not that you should type square brackets at that

> &gt;&gt;&gt; all\_users
>
> \['qiwsir', 'github', 'io', 'algorithm'\]
>
> &gt;&gt;&gt; all\_users.pop\(\) \#list.pop\(\[i\]\),圆括号里面是\[i\]，表示这个序号是可选的
>
> 'algorithm' \#如果不写，就如同这个操作，默认删除最后一个，并且将该结果返回
>
> &gt;&gt;&gt; all\_users
>
> \['qiwsir', 'github', 'io'\]
>
> &gt;&gt;&gt; all\_users.pop\(1\) \#指定删除编号为1的元素"github"
>
> 'github'

**1.3range\(start,stop\)生成数字list**

range\(start, stop\[, step\]\)是一个内置函数。

从这段话，我们可以得出关于range\(\)函数的以下几点：

这个函数可以创建一个数字元素组成的列表。

这个函数最常用于for循环（关于for循环，马上就要涉及到了）

函数的参数必须是整数，默认从0开始。返回值是类似\[start, start + step, start + 2\*step,

...\]的列表。

step默认值是1。如果不写，就是按照此值。

如果step是正数，返回list的最最后的值不包含stop值，即start+istep这个值小于stop；如果step是负数，start+istep的值大于stop。

step不能等于零，如果等于零，就报错。

在实验开始之前，再解释range\(start,stop\[,step\]\)的含义：

start：开始数值，默认为0,也就是如果不写这项，就是认为start=0

stop：结束的数值，必须要写的。

step：变化的步长，默认是1,也就是不写，就是认为步长为1。坚决不能为0

如：

> &gt;&gt;&gt; range\(9\) \#stop=9，别的都没有写，含义就是range\(0,9,1\)
>
> \[0, 1, 2, 3, 4, 5, 6, 7, 8\] \#从0开始，步长为1,增加，直到小于9的那个数
>
> &gt;&gt;&gt; range\(0,9\)
>
> \[0, 1, 2, 3, 4, 5, 6, 7, 8\]
>
> &gt;&gt;&gt; range\(0,9,1\)
>
> \[0, 1, 2, 3, 4, 5, 6, 7, 8\]
>
> &gt;&gt;&gt; range\(1,9\) \#start=1
>
> \[1, 2, 3, 4, 5, 6, 7, 8\]
>
> &gt;&gt;&gt; range\(0,9,2\)
>
> \[0, 2, 4, 6, 8\]

解释一下range\(0,9,2\)

* 如果是从0开始，步长为1,可以写成range\(9\)的样子，但是，如果步长为2，写成

range\(9,2\)的样子，计算机就有点糊涂了，它会认为start=9,stop=2。所以，在步长不为1

的时候，切忌，要把start的值也写上。

* start=0,step=2,stop=9.list中的第一个值是start=0,第二个值是start+1step=2（注意，这里

是1，不是2，不要忘记，前面已经讲过，不论是list还是str，对元素进行编号的时候，都

是从0开始的），第n个值就是start+\(n-1\)step。直到小于stop前的那个值。

思考一个问题，现在有一个列表，比如是

\["I","am","a","pythoner","I","am","learning","it","with","qiwsir"\],要得到这个list的所有序号组成的

list，但是不能一个一个用手指头来数。怎么办？

请沉思两分钟之后，自己实验一下，然后看下面。

> &gt;&gt;&gt; pythoner
>
> \['I', 'am', 'a', 'pythoner', 'I', 'am', 'learning', 'it', 'with', 'qiwsir'\]
>
> &gt;&gt;&gt; py\_index = range\(len\(pythoner\)\) \#以len\(pythoner\)为stop的值
>
> &gt;&gt;&gt; py\_index
>
> \[0, 1, 2, 3, 4, 5, 6, 7, 8, 9\]

再用手指头指着pythoner里面的元素，数一数，是不是跟结果一样。

**1.4list排序**

> list.sort\(cmp=None, key=None, reverse=False\)
>
> sorted\(iterable\[, cmp\[, key\[, reverse\]\]\]\)
>
> &gt;&gt;&gt; number = \[1,4,6,2,9,7,3\]
>
> &gt;&gt;&gt; number.sort\(\)
>
> &gt;&gt;&gt; number
>
> \[1, 2, 3, 4, 6, 7, 9\]
>
> &gt;&gt;&gt; number = \[1,4,6,2,9,7,3\]
>
> &gt;&gt;&gt; number
>
> \[1, 4, 6, 2, 9, 7, 3\]
>
> &gt;&gt;&gt; sorted\(number\)
>
> \[1, 2, 3, 4, 6, 7, 9\]
>
> &gt;&gt;&gt; number = \[1,4,6,2,9,7,3\]
>
> &gt;&gt;&gt; number
>
> \[1, 4, 6, 2, 9, 7, 3\]
>
> &gt;&gt;&gt; number.sort\(reverse=True\) \#开始实现倒序
>
> &gt;&gt;&gt; number
>
> \[9, 7, 6, 4, 3, 2, 1\]
>
> &gt;&gt;&gt; number = \[1,4,6,2,9,7,3\]
>
> &gt;&gt;&gt; number
>
> \[1, 4, 6, 2, 9, 7, 3\]
>
> &gt;&gt;&gt; sorted\(number,reverse=True\)
>
> \[9, 7, 6, 4, 3, 2, 1\]

**1.5查找list方法**

> help\(list\)

**1.6list和str比较**

相同点

都属于序列类型的数据

所谓序列类型的数据，就是说它的每一个元素都可以通过指定一个编号，行话叫做“偏移量”的

方式得到，而要想一次得到多个元素，可以使用切片。偏移量从0开始，总元素数减1结束。

例如：

> &gt;&gt;&gt; welcome\_str = "Welcome you"
>
> &gt;&gt;&gt; welcome\_str\[0\]
>
> 'W'
>
> &gt;&gt;&gt; welcome\_str\[1\]
>
> 'e'
>
> &gt;&gt;&gt; welcome\_str\[len\(welcome\_str\)-1\]
>
> 'u'
>
> &gt;&gt;&gt; welcome\_str\[:4\]
>
> 'Welc'
>
> &gt;&gt;&gt; a = "python"
>
> &gt;&gt;&gt; a\*3
>
> 'pythonpythonpython'
>
> &gt;&gt;&gt; git\_list = \["qiwsir","github","io"\]
>
> &gt;&gt;&gt; git\_list\[0\]
>
> 'qiwsir'
>
> &gt;&gt;&gt; git\_list\[len\(git\_list\)-1\]
>
> 'io'
>
> &gt;&gt;&gt; git\_list\[0:2\]
>
> \['qiwsir', 'github'\]
>
> &gt;&gt;&gt; b = \['qiwsir'\]
>
> &gt;&gt;&gt; b\*7
>
> \['qiwsir', 'qiwsir', 'qiwsir', 'qiwsir', 'qiwsir', 'qiwsir', 'qiwsir'\]

对于此类数据，下面一些操作是类似的：

> &gt;&gt;&gt; first = "hello,world"
>
> &gt;&gt;&gt; welcome\_str
>
> 'Welcome you'
>
> &gt;&gt;&gt; first+","+welcome\_str \#用+号连接str
>
> 'hello,world,Welcome you'
>
> &gt;&gt;&gt; welcome\_str \#原来的str没有受到影响，即上面的+号连接后从新生成了一个字符串
>
> 'Welcome you'
>
> &gt;&gt;&gt; first
>
> 'hello,world'
>
> &gt;&gt;&gt; language = \['python'\]
>
> &gt;&gt;&gt; git\_list
>
> \['qiwsir', 'github', 'io'\]
>
> &gt;&gt;&gt; language + git\_list \#用+号连接list，得到一个新的list
>
> \['python', 'qiwsir', 'github', 'io'\]
>
> &gt;&gt;&gt; git\_list
>
> \['qiwsir', 'github', 'io'\]
>
> &gt;&gt;&gt; language
>
> \['python'\]
>
> &gt;&gt;&gt; len\(welcome\_str\) \#得到字符数
>
> 11
>
> &gt;&gt;&gt; len\(git\_list\) \#得到元素数
>
> 3

区别：

list和str的最大区别是：list是可以改变的，str不可变。这个怎么理解呢

如果要修改一个str，不得不这样。

> &gt;&gt;&gt; welcome\_str
>
> 'Welcome you'
>
> &gt;&gt;&gt; welcome\_str\[0\]+"E"+welcome\_str\[2:\] \#从新生成一个str
>
> 'WElcome you'
>
> &gt;&gt;&gt; welcome\_str \#对原来的没有任何影响
>
> 'Welcome you'

其实，在这种做法中，相当于从新生成了一个str。

**1.7list与str的转化**

str.split\(\)

这个内置函数实现的是将str转化为list。其中str=""是分隔符。

> &gt;&gt;&gt; line = "Hello.I am qiwsir.Welcome you."
>
> &gt;&gt;&gt; line.split\("."\) \#以英文的句点为分隔符，得到list
>
> \['Hello', 'I am qiwsir', 'Welcome you', ''\]
>
> &gt;&gt;&gt; line.split\(".",1\) \#这个1,就是表达了上文中的：If maxsplit is given, at most maxsplit splits are done.
>
> \['Hello', 'I am qiwsir.Welcome you.'\]
>
> &gt;&gt;&gt; name = "Albert Ainstain" \#也有可能用空格来做为分隔符
>
> &gt;&gt;&gt; name.split\(" "\)
>
> \['Albert', 'Ainstain'\]
>
> &gt;&gt;&gt; s = "I am, writing\npython\tbook on line" \#这个字符串中有空格，逗号，换行\n，tab缩进\t 符号
>
> &gt;&gt;&gt; print s \#输出之后的样式
>
> I am, writing
>
> python book on line
>
> &gt;&gt;&gt; s.split\(\) \#用split\(\),但是括号中不输入任何参数
>
> \['I', 'am,', 'writing', 'python', 'book', 'on', 'line'\]

如果split\(\)不输入任何参数，显示就是见到任何分割符号，就用其分割了。

"\[sep\]".join\(list\)

> join可以说是split的逆运算，举例：
>
> &gt;&gt;&gt; name
>
> \['Albert', 'Ainstain'\]
>
> &gt;&gt;&gt; "".join\(name\) \#将list中的元素连接起来，但是没有连接符，表示一个一个紧邻着
>
> 'AlbertAinstain'
>
> &gt;&gt;&gt; ".".join\(name\) \#以英文的句点做为连接分隔符
>
> 'Albert.Ainstain'
>
> &gt;&gt;&gt; " ".join\(name\) \#以空格做为连接的分隔符
>
> 'Albert Ainstain'



