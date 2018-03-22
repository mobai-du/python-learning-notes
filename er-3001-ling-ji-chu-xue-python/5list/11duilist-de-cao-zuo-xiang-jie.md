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

&gt;&gt;&gt; all\_users.insert\(1,"\[[http://"\]\(http://"\)\](http://"]%28http://"%29\)\)

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

