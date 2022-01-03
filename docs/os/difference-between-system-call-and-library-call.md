# 系统调用和库调用的区别

> 原文:[https://www . geesforgeks . org/系统调用和库调用的区别/](https://www.geeksforgeeks.org/difference-between-system-call-and-library-call/)

**1。** [**系统调用**](https://www.geeksforgeeks.org/introduction-of-system-call/) **:**
计算机系统中有两种模式一种是**用户模式**，另一种是**内核模式**。在计算机系统中，有不同类型的进程在计算机系统上运行。当用户运行一个应用程序时，它被称为处于用户模式或计算机处于用户模式。当需要硬件资源时，进程向内核发送请求以获得进程访问权限，然后计算机进入内核模式。这些请求通过使用系统调用来发送。计算机经常在这两种模式之间切换。每当任务完成时，计算机从内核模式返回到用户模式。这种过渡模式称为**上下文切换。**

**2。库调用:**
库调用是一种使用编程库中定义的特定函数的请求。库文件包含代码数据文件、打包成一个文件使用的目标文件。要进行库调用，应首先导入库。库调用可能依赖于系统调用来完成任务。

**系统调用和库调用的区别:**

<figure class="table">

| **序列号** | **系统调用**

 | **库调用** |
| 1. | 系统调用是程序发出的进入内核模式访问进程的请求.. | 库调用是程序发出的访问编程库中定义的库函数的请求。 |
| 2. | 在内核模式下，内存和硬件资源可以直接访问程序。 | 在用户模式下，程序不能直接访问内存和硬件资源。 |
| 3. | 在系统调用中，模式被执行或从用户模式切换到内核模式。 | 在库调用中，该模式仅在用户模式下执行。 |
| 4. | 在系统调用中，执行进程的速度比库调用慢，因为有一种称为上下文切换的转换模式。 | 在库调用中，执行进程的速度比系统调用快，因为没有上下文切换模式。 |
| 5. | 系统调用是内核提供的进入内核模式访问硬件资源的功能。 | 库调用是由编程库提供的执行任务的函数。 |
| 6. | 系统调用是内核的入口点，因此它们没有链接到程序。 | 库函数链接到您的程序中。 |
| 7. | 系统调用是不可移植的。 | 库调用是可移植的。 |
| 8. | 系统调用比库调用拥有更多的特权，因为它以监督模式运行。 | 库调用比系统调用权限小，因为它仅在用户模式下运行。 |
| 9. | 系统调用由系统提供，并由系统内核执行。 | 库调用包括 ANSI C 标准库。 |
| 10. | 在系统调用中，所有函数都是内核的一部分。 | 在库调用中，所有库函数都是编程语言标准库文件的一部分。 |
| 11. | 每当程序需要内存或硬件资源时，它就直接向内核发送请求，通过使用系统调用来获取进程访问权。 | 每当程序员或开发人员使用特定的库函数时，程序员必须首先通过在程序中包含头文件来调用库函数。预处理器(#)指令有助于包含头文件。一些有用的头文件如下1.#包括<stdio.h></stdio.h>2.#包括<math.h></math.h>3.#包括 |
| 12. | 系统调用的例子有–1.叉子()2.exec() | 库调用示例有–1.fopen()2\. fclose()3 .扫描()4.printf() |

</figure>