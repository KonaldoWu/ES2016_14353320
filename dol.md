##DOL初体验
                                          --by吴云柯（14353320） using markdown
* example1的分析
     
       我们首先看到src里面有这些文件，其中consumer是消费者，generator是生产者
![](http://oepww4mce.bkt.clouddn.com/16-10-11/58898245.jpg)
 
 首先让我们来看一看生产者的c文件里讲了些什么东西
 
![](http://oepww4mce.bkt.clouddn.com/16-10-11/92163089.jpg)
 如图，首先是一个init即初始化函数，首先将当前位置初始化为0，然后设置生产者长度为length。
 然后对于fire函数，它始终就是在检测index与len的大小关系，如果index大小小于len，即当前位置小于生产长度，就将x写到generator的端口“PORT_OUT"上，如果index大于len了，就终止进程。
 
 接下来让我们理解一下消费者是干些什么
![](http://oepww4mce.bkt.clouddn.com/16-10-11/79212385.jpg)
 定义和生产者差不多我就不赘述了，对于fire，同样是比较大小，若符合条件，就读取PORT_IN端口的数据，然后输出，最后来个index+1，跳出这个循环就终止程序
 修改后的结果就是这样
![](http://oepww4mce.bkt.clouddn.com/16-10-11/84556164.jpg)

dot图就是这样
![](http://oepww4mce.bkt.clouddn.com/16-10-11/34404630.jpg)
然后可以看到example1.xml里面对connect有一些定义
![](http://oepww4mce.bkt.clouddn.com/16-10-11/34623840.jpg)
generator有一个端口是output，consumer有一个端口是input，而square有两个，同时有输入和输出
要注意，每个单位和线条都分左右端口，例如generator的右端口连到C1左端口，C1的右端口连到square的左端口

* example2的分析
其实example2的生产者和消费者代码和1基本一样，区别就在于example2架构中有三个square模块。
主要关键技术就大概是用了个迭代吧。附上结果图，没什么好特别讲的
![](http://oepww4mce.bkt.clouddn.com/16-10-11/21747600.jpg)

* 感想
 
      这次还是主要熟悉一下dol的使用咯，这个dol图还是蛮新奇的。虽然实验比较简单，但我还是逐条代码看了，感觉对称的结构代码有点HTML的画风。有一点发现都在上面讲了，完成过程中改三次方的时候，一开始没有变化，问了TA才知道有时候系统没有识别到更改，最好还是先把build那边的文件一个文件先删掉，重新build一下。总之还是比较顺利也是比较有趣。