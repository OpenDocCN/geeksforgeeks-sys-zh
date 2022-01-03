# 中断和异常的区别

> 原文:[https://www . geesforgeks . org/中断和异常之间的区别/](https://www.geeksforgeeks.org/difference-between-interrupt-and-exception/)

先决条件–[中断和异常](https://www.geeksforgeeks.org/interrupts-and-exceptions/)
中断是异常的一个类别。有 4 类异常-中断、陷阱、故障和中止。尽管中断属于例外，但它们之间仍有许多不同之处。

在任何计算机中，在程序的正常执行过程中，都有可能发生导致中央处理器暂时停止的事件。像这样的事件叫做中断。中断可能由软件或硬件故障引起。硬件中断称为中断，而软件中断称为异常。一旦中断被引发，控制就被转移到一个特殊的子程序，叫做中断服务程序(ISR)，它可以处理由中断引发的情况。

**什么是陷阱、故障和中止？**

1.  **Trap–**
    这是一种典型的同步中断，由异常情况(例如断点、被零除、无效内存访问)引起。
2.  **故障–**
    故障异常在客户端应用程序中用于捕获契约指定的 SOAP 故障。通过简单的异常消息，您无法识别异常的原因，这就是为什么故障异常是有用的。
3.  **异常中止–**
    这是一种在指令提取导致错误时发生的异常。

**什么是中断？**
中断一词通常用于硬件中断。它们是由外部硬件事件引起的程序控制中断。这里，外部是指在 CPU 外部。硬件中断通常来自许多不同的来源，如定时器芯片、外围设备(键盘、鼠标等)。)，I/O 端口(串行、并行等)。)，磁盘驱动器，CMOS 时钟，扩展卡(声卡，显卡等)。这意味着硬件中断几乎不会因为与正在执行的程序相关的事件而发生。

**示例–**
用户在键盘上按键或内部硬件定时器超时等事件会引发这种中断，并通知 CPU 某个设备需要注意。在这种情况下，中央处理器将停止它正在做的任何事情(即暂停当前程序)，提供设备所需的服务，并返回正常程序。当硬件中断发生并且中央处理器启动中断服务时，其他硬件中断被禁用(例如在 80×86 机器中)。如果您需要在 ISR 运行时发生其他硬件中断，您需要通过清除中断标志(使用 sti 指令)来明确做到这一点。在 80×86 机器中，清除中断标志只会影响硬件中断。

**什么是异常？**
异常是软件中断，可以识别为特殊的处理程序例程。异常可以被识别为自动出现的陷阱。通常，没有与异常相关联的特定指令(陷阱是使用特定指令生成的)。因此，异常是由于程序执行过程中出现的“异常”情况而发生的。

**示例–**
除以零，执行非法操作码或与内存相关的故障可能会导致异常。每当出现异常时，中央处理器都会暂时挂起正在执行的程序，并启动中断服务程序。ISR 将包含如何处理异常。它可以纠正问题，或者如果不可能，它可以通过打印适当的错误信息来正常中止程序。虽然特定的指令不会导致异常，但异常总是由指令引起的。例如，除以零错误只能在除法指令执行期间发生。

**中断和异常的区别:**

<center>

| 中断 | 例外 |
| --- | --- |
| 这些是硬件中断。 | 这些是软件中断。 |
| 硬件中断的出现通常会禁用其他硬件中断。 | 就“例外”而言，这不是真实的情况。 |
| 这些是异步的外部服务请求(像键盘或打印机需要服务)。 | 这些是基于异常事件的同步内部服务请求(想想非法指令、非法地址、溢出等)。 |
| 由于异步，中断可以发生在程序的任何地方。 | 由于是同步的，当你的程序中出现异常事件时，比如被零除或非法内存位置，就会出现异常。 |
| 这些都是正常事件，不应该干扰电脑的正常运行。 | 这些都是异常事件，通常会导致程序终止 |

</center>