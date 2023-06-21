# 交换机和网关的区别

> 原文:[https://www . geeksforgeeks . org/交换机和网关的区别/](https://www.geeksforgeeks.org/difference-between-switch-and-gateway/)

先决条件–[网络设备](https://www.geeksforgeeks.org/network-devices-hub-repeater-bridge-switch-router-gateways/)

**1。交换机:**
交换机是一个多端口的桥，有一个缓冲器和一个可以提高其效率和性能的设计。它是一个数据链路层设备。交换机可以在转发数据之前执行错误检查，这使得它非常高效，因为它不会转发有错误的数据包，而是选择性地仅将好的数据包转发到正确的端口。换句话说，交换机划分了主机的冲突域。

**2。网关:**
网关是连接两个网络的通道，这两个网络可以在不同的网络模型上工作。它基本上充当系统之间的信使代理，从一个系统获取数据，解释数据并将其传输到另一个系统。它也被称为协议转换器。它可以在任何网络层运行。它比开关更复杂。

**交换机和网关的区别:**

<center>

| 转换 | 门 |
| --- | --- |
| 它作为网络之间的多端口桥梁。 | 它是两个网络之间的通道。 |
| 它在数据链路层工作。 | 它适用于所有网络层。 |
| 它在转发数据包之前执行错误检查。 | 它不执行错误检查。 |
| 它不能作为协议转换器工作。 | 当它作为协议转换器工作时。 |
| 交换机中提供包过滤。 | 网关中不提供包过滤。 |
| 它不太复杂。 | 它比开关更复杂。 |
| 它连接在同一网络模型上工作的设备。 | 它连接了在不同模型上工作的两个网络。 |
| 数据包的格式不变。 | 数据包格式已更改。 |

</center>