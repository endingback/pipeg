# 策略模式

## 概述

本节将用两种算法把列表中的元素输出到表格里面。列表中的元素个数不限，而用户可以指定表格的行数。

- 第一种算法将会产生HTML页面。
- 第二种算法则会以纯文本形式输出。


## 切换算法的办法

- tabulator1.py

创建 Layout 类，令其实例接受 Tabulator 实例，再由该实例负责将列表中的元素排布在表格里。程序就是这么做的。

- tabulator2.py

不把制表算法表示成 Tabulator 实例，而是把它们做出 Tabulator 子类的静态方法，这样就不用把 Tabulator 实例传给Layout了，只需传入含有制表算法的 Tabulator 子类即可。


## 总结

现实环境中各种算法其代码与性能也许有很大差异，而策略模式则使用户能够根据需求来选择最为合适的方案。

把各种算法当成 callable 安插在程序里是非常容易的事，因为 callable 在 Python 语言是“一等对象”，也就是说，我们可以像其他对象那样，在函数间传递 callable，或将其存放在集合里。


