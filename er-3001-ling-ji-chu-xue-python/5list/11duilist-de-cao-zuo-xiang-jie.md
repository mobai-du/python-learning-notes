**1.1向list中插入一个元素**

这种改变的含义只它的大小即所容纳元素的  
个数以及元素内容，可以随时直接修改，而不用进行转换。这和str有着很大的不同。对于  
str，就不能进行字符的追加。请看官要注意比较，这也是str和list的重要区别。  
与list.append\(x\)类似，list.insert\(i,x\)也是对list元素的增加。只不过是可以在任何位置增加一个  
元素。

&gt;&gt;&gt; all\_users

\['qiwsir', 'github', 'io'\]

&gt;&gt;&gt; all\_users.insert\("python"\) \#list.insert\(i,x\),要求有两个参数，少了就报错

Traceback \(most recent call last\):

File "&lt;stdin&gt;", line 1, in &lt;module&gt;

TypeError: insert\(\) takes exactly 2 arguments \(1 given\)

&gt;&gt;&gt; all\_users.insert\(0,"python"\)

&gt;&gt;&gt; all\_users

\['python', 'qiwsir', 'github', 'io'\]

&gt;&gt;&gt; all\_users.insert\(1,"\[\[\[\[\[\[\[[http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\]\(http://"\]\(http://"\)\]\(http://"\]\(http://"\)\)\)\)\)\)\)\](http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29]%28http://"]%28http://"%29]%28http://"]%28http://"%29%29%29%29%29%29%29\)\)

&gt;&gt;&gt; all\_users

\['python', 'http://', 'qiwsir', 'github', 'io'\]

&gt;&gt;&gt; length = len\(all\_users\)

&gt;&gt;&gt; length

5

&gt;&gt;&gt; all\_users.insert\(length,"algorithm"\)

&gt;&gt;&gt; all\_users

\['python', 'http://', 'qiwsir', 'github', 'io', 'algorithm'\]

list.insert\(i,x\),将新的元素x 插入到原list中的list\[i\]前面

如果i==len\(list\)，意思是在后面追加，就等同于list.append\(x\)

**1.2删除list中的元素**

list.remove\(x\)

Remove the first item from the list whose value is x. It is an error if there is no such

item.

a=\["abc",123,8\]

a.remove\(8\)

a\["abc",123\]

list.pop\(\[i\]\)

Remove the item at the given position in the list, and return it. If no index is

specified, a.pop\(\) removes and returns the last item in the list. \(The square

brackets around the i in the method signature denote that the parameter is

optional, not that you should type square brackets at that

&gt;&gt;&gt; all\_users

\['qiwsir', 'github', 'io', 'algorithm'\]

&gt;&gt;&gt; all\_users.pop\(\) \#list.pop\(\[i\]\),圆括号里面是\[i\]，表示这个序号是可选的

'algorithm' \#如果不写，就如同这个操作，默认删除最后一个，并且将该结果返回

&gt;&gt;&gt; all\_users

\['qiwsir', 'github', 'io'\]

&gt;&gt;&gt; all\_users.pop\(1\) \#指定删除编号为1的元素"github"

'github'

**1.3range\(start,stop\)生成数字list**

range\(start, stop\[, step\]\)是一个内置函数。

从这段话，我们可以得出关于range\(\)函数的以下几点：

这个函数可以创建一个数字元素组成的列表。

这个函数最常用于for循环（关于for循环，马上就要涉及到了）

函数的参数必须是整数，默认从0开始。返回值是类似\[start, start + step, start + 2\*step,

...\]的列表。

step默认值是1。如果不写，就是按照此值。

零基础学Python

有容乃大的list\(4\) 84

如果step是正数，返回list的最最后的值不包含stop值，即start+istep这个值小于stop；如

果step是负数，start+istep的值大于stop。

step不能等于零，如果等于零，就报错。

在实验开始之前，再解释range\(start,stop\[,step\]\)的含义：

start：开始数值，默认为0,也就是如果不写这项，就是认为start=0

stop：结束的数值，必须要写的。

step：变化的步长，默认是1,也就是不写，就是认为步长为1。坚决不能为0











