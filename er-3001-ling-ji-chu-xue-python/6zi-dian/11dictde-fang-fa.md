**1.1嵌套**

> &gt;&gt;&gt; a\_list = \[\[1,2,3\],\[4,5\],\[6,7\]\]
>
> &gt;&gt;&gt; a\_list\[1\]\[1\]
>
> 5
>
> &gt;&gt;&gt; a\_dict = {1:{"name":"qiwsir"},2:"python","email":"qiwsir@gmail.com"}
>
> &gt;&gt;&gt; a\_dict
>
> {1: {'name': 'qiwsir'}, 2: 'python', 'email': 'qiwsir@gmail.com'}
>
> &gt;&gt;&gt; a\_dict\[1\]\['name'\] \#一个嵌套的dict访问其值的方法：一层一层地写出键
>
> 'qiwsir'

**2.1获取键、值**

&gt;&gt;&gt; website = {1:"google","second":"baidu",3:"facebook","twitter":4}

&gt;&gt;&gt;\#用d.keys\(\)的方法得到dict的所有键，结果是list

&gt;&gt;&gt; website.keys\(\)

\[1, 'second', 3, 'twitter'\]

> &gt;&gt;&gt;\#用d.values\(\)的方法得到dict的所有值，如果里面没有嵌套别的dict，结果是list
>
> &gt;&gt;&gt; website.values\(\)
>
> \['google', 'baidu', 'facebook', 4\]
>
> &gt;&gt;&gt;\#用items\(\)的方法得到了一组一组的键值对，
>
> &gt;&gt;&gt;\#结果是list，只不过list里面的元素是元组
>
> &gt;&gt;&gt; website.items\(\)
>
> \[\(1, 'google'\), \('second', 'baidu'\), \(3, 'facebook'\), \('twitter', 4\)\]

for循环得到键、值

> &gt;&gt;&gt; for key in website.keys\(\):
>
> ... print key,type\(key\)
>
> ...
>
> 1 &lt;type 'int'&gt;
>
> second &lt;type 'str'&gt;
>
> 3 &lt;type 'int'&gt;
>
> twitter &lt;type 'str'&gt;
>
> &gt;&gt;&gt;\#下面的方法和上面的方法是一样的
>
> &gt;&gt;&gt; for key in website:
>
> ... print key,type\(key\)
>
> ...
>
> 1 &lt;type 'int'&gt;
>
> second &lt;type 'str'&gt;
>
> 3 &lt;type 'int'&gt;
>
> twitter &lt;type 'str'&gt;

以下两种方法等效：

> &gt;&gt;&gt; for value in website.values\(\):
>
> ... print value
>
> ...
>
> google
>
> baidu
>
> facebook
>
> 4
>
> &gt;&gt;&gt; for key in website:
>
> ... print website\[key\]
>
> ...
>
> google
>
> baidu
>
> facebook
>
> 4

3.1删除键

删除键值对的方法有两个，但是两者有一点区别

> &gt;&gt;&gt;\#d.pop\(key\)，根据key删除相应的键值对，并返回该值
>
> &gt;&gt;&gt; new\_web.pop\('second'\)
>
> 'baidu'
>
> &gt;&gt;&gt; del new\_web\[3\]　 \#没有返回值，如果删除键不存在，返回错误
>
> &gt;&gt;&gt; new\_web
>
> {1: 'google', 'twitter': 4}
>
> &gt;&gt;&gt; del new\_web\[9\]
>
> Traceback \(most recent call last\):
>
> File "&lt;



