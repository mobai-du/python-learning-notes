想得到1到9的每个整数的平方，并且将结果放在list中打印出来

> &gt;&gt;&gt; power2 = \[\]
>
> &gt;&gt;&gt; for i in range\(1,10\):
>
> ... power2.append\(i\*i\)
>
> ...
>
> &gt;&gt;&gt; power2
>
> \[1, 4, 9, 16, 25, 36, 49, 64, 81\]

python有一个非常有意思的功能，就是list解析，就是这样的：

> &gt;&gt;&gt; squares = \[x\*\*2 for x in range\(1,10\)\]
>
> &gt;&gt;&gt; squares
>
> \[1, 4, 9, 16, 25, 36, 49, 64, 81\]

找出100以内的能够被3整除的正整数。

用list解析

> &gt;&gt;&gt; aliquot = \[n for n in range\(1,100\) if n%3==0\]
>
> &gt;&gt;&gt; aliquot
>
> \[3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36, 39, 42, 45, 48, 51, 54, 57, 60, 63, 66, 69, 72,

**enumerate**

这是一个有意思的内置函数，本来我们可以通过for i in range\(len\(list\)\)的方式得到一个list的每

个元素编号，然后在用list\[i\]的方式得到该元素。如果要同时得到元素编号和元素怎么办？就

是这样了:

> week=\["monday","sunday","friday"\]
>
> &gt;&gt;&gt; for i in range\(len\(week\)\):
>
> ... print week\[i\]+' is '+str\(i\) \#注意，i是int类型，如果和前面的用+连接，必须是str类型
>
> ...
>
> monday is 0
>
> sunday is 1
>
> friday is 2

python中提供了一个内置函数enumerate，能够实现类似的功能

> week=\["monday","sunday","friday"\]
>
> &gt;&gt;&gt; for \(i,day\) in enumerate\(week\):
>
> ... print day+' is '+str\(i\)
>
> ...
>
> monday is 0
>
> sunday is 1
>
> friday is 2



