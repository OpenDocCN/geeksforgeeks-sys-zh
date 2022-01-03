# fork()和 vfork()

的区别

> 原文:[https://www . geesforgeks . org/fork-and-vfork 的区别/](https://www.geeksforgeeks.org/difference-between-fork-and-vfork/)

**1。 [fork()](https://www.geeksforgeeks.org/fork-system-call/) :**
Fork()是用于创建新流程的系统调用。由 fork()系统调用创建的新进程称为子进程，调用 fork()系统调用的进程称为父进程。子进程的代码与其父进程的代码相同。一旦创建了子进程，父进程和子进程都从 fork()之后的下一条语句开始执行，并且两个进程同时执行。

**2。vfork() :**
Vfork()也是系统调用，用来创建新的流程。由 vfork()系统调用创建的新进程称为子进程，调用 vfork()系统调用的进程称为父进程。子进程的代码与其父进程的代码相同。子进程暂停父进程的执行，直到子进程完成其执行，因为两个进程共享相同的地址空间。

**fork()和 vfork()的区别:**

<center>

| 没有。 | FORK() | VFORK() |
| --- | --- | --- |
| 1. | 在 fork()系统调用中，子进程和父进程有单独的内存空间。 | 在 vfork()系统调用中，子进程和父进程共享相同的地址空间。 |
| 2. | 子进程和父进程同时执行。 | 一旦执行了子进程，父进程就开始执行。 |
| 3. | fork()系统调用使用写时复制作为替代方法。 | 而 vfork()系统调用不使用写时复制。 |
| 4. | 在 fork()系统调用中，子进程不会挂起父进程的执行。 | 子进程在 vfork()系统调用中挂起父进程的执行。 |
| 5. | 一个进程的页面不受另一个进程的页面影响。 | 一个进程的页面受另一个进程的页面影响。 |
| 6. | fork()系统调用使用较多。 | vfork()系统调用使用较少。 |
| 7. | 地址空间被浪费了。 | 地址空间没有浪费。 |
| 8. | 如果子进程改变了地址空间中的页面，它对父进程是不可见的。 | 如果子进程改变了地址空间中的页面，它对父进程是可见的。 |

</center>