## 2

### 操作系统概论

如果你正在上一门操作系统的本科课程，你应该已经对计算机程序在运行时的究竟做了什么有了一定的了解。如果没有，这本书（以及其相应的课程）对你来说将会非常困难——因此你也许应该停止阅读这本书，或者跑到最近的书店，在继续阅读前快速的掌握必要的背景知识。（由 Patt 和 Patel 所著的[PP03]，特别是由 Bryant 与 O’Hallaron 合著的[BOH10]都是极好的书）。

所以，当一个程序运行时究竟发生了什么呢？

嗯，运行的程序仅仅做了一件非常简单的事：它在执行指令。处理器每秒钟从内存中获取着着数百万（现在甚至数十亿）条指令，对其进行解码（即找出它对应的指令），并执行指令（即做应该做的事，比如说两数求和、访问内存、检查条件、跳转到某个函数等等）。当它执行完这条指令后，处理器便跳转到下一条指令…直到程序执行彻底完成。

因此，我们刚刚描述了冯·诺依曼（Von Neumann）计算模型的基础。听起来很简单对吗？但是在这个课堂上，我们将了解到当一个程序运行时，还有许多令人激动的事情正在进行，他们的主要目的是让系统更加的易用。

事实上，有一个软件负责使程序更加容易的运行（甚至允许您在表面上同时运行许多程序），允许程序去共享内存，允许程序与设备进行交互和其他许许多多的类似的有趣的事。这个软件叫做操作系统（operating system, OS），它作为负责确保系统以易于使用的方式正确和高效的运行。

核心的问题：如何去虚拟化资源（virtualize resources）

在本书中我们将回答的一个核心问题非常简单：操作系统是如何虚拟化资源的呢？这是我们问题的核心。为什么操作系统会这样做并不是主要的问题，因为答案应该是显而易见的：它使得系统更易用。
