1.：变量无类型，对象有类型

在python中，如果要使用一个变量，不需要提前声明，只需要在用的时候，给这个变量赋值

即可。这里特别强调，只要用一个变量，就要给这个变量赋值。



在前面讲述中，我提出了一个类比，就是变量通过一根线，连着对象（具体就可能是一个

int/list等），这个类比被很多人接受了，算是我老齐的首创呀。那么，如果要用一种严格的语

言来描述，变量可以理解为一个系统表的元素，它拥有过指向对象的命名空间。太严肃了，

不好理解，就理解我那个类比吧。变量就是存在系统中的一个东西，这个东西有一种能力，

能够用一根线与某对象连接，它能够钓鱼。

对象呢？展开想象。在机器的内存中，系统分配一个空间，这里面就放着所谓的对象，有时

候放数字，有时候放字符串。如果放数字，就是int类型，如果放字符串，就是str类型。

接下来的事情，就是前面说的变量用自己所拥有的能力，把对象和自己连接起来（指针连接

对象空间），这就是引用。引用完成，就实现了赋值。

看到上面的图了吧，从图中就比较鲜明的表示了变量和对象的关系。所以，严格地将，只有

放在内存空间中的对象（也就是数据）才有类型，而变量是没有类型的。这么说如果还没有

彻底明白，就再打一个比喻：变量就好比钓鱼的人，湖水里就好像内存，里面有好多鱼，有

各种各样的鱼，它们就是对象。钓鱼的人（变量）的任务就是用某种方式（鱼儿引诱）把自

己和鱼通过鱼线连接起来。那么，鱼是有类型的，有鲢鱼、鲫鱼、带鱼（带鱼也跑到湖水了

了，难道是淡水带鱼？呵呵，就这么扯淡吧，别较真），钓鱼的人（变量）没有这种类型，

他钓到不同类型的鱼。

