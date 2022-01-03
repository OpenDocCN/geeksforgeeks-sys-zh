# 南桥及其功能

> 原文:[https://www . geesforgeks . org/south-bridge-and-it-functions/](https://www.geeksforgeeks.org/south-bridge-and-its-functions/)

[南桥](https://www.geeksforgeeks.org/motherboard-parts-south-bridge/)通常位于主板下缘附近。它是芯片组中速度较低的组件，并且一直是单个芯片。不同的北桥芯片可以与相同的南桥组件一起使用。芯片组的这种模块化设计为主板制造商提供了更低的成本和更大的灵活性。南桥的主要功能是作为**外围控制器**。

**南桥功能:**
外围控制器(南桥)主要功能包括:

1.  **I/O 总线控制–**
    大多数现代计算机使用两条总线:工业标准架构(ISA)总线用于速度较慢的外围设备，并与较旧的组件兼容，PCI 是用于硬盘、显卡和其他高速设备的高速“本地总线”。南桥控制这些总线，并在它们之间以及处理器和存储器之间传输信息。南桥的能力决定了什么样的总线系统可以支持，他们可以以什么速度运行，以及他们可以有什么额外的功能。
2.  **总线桥–**
    桥是一个网络术语，指的是连接两个不同网络并将信息从一个网络上的计算机传递到另一个网络上的计算机的硬件，反之亦然。以类似的方式，芯片组必须使用总线桥将它控制的不同系统总线类型连接在一起。其中最常见的是 PCI-ISA 桥，它将两条不同总线上的设备连接在一起。南桥芯片单独或通过 PCI 到 ISA 桥芯片维护 ISA 总线之间的桥。
3.  **中断控制器–**
    中断控制器提供了输入/输出设备请求处理器注意处理数据传输的手段。南桥芯片通过集成中断控制器的所有功能取代了 PIC 芯片。
4.  **DMA 控制器支持–**
    南桥提供直接内存访问(DMA)控制器支持，为设备提供了一种无需处理器干预，直接在内存之间传递信息的方式。
5.  **ATA/IDE 接口–**
    南桥芯片通常提供双 IDE 端口，用于连接多达和磁盘，每个通道两个。
6.  **USB 端口–**
    南桥芯片也控制主板上的 USB 支持。
7.  **电源管理器–**
    南桥监控电脑不同部分的总耗电量，以节省电力。
8.  **即插即用支持–**
    即插即用(PnP)是一种规范，允许 BIOS 和 OS 自动检测系统中新设备的安装，并自动为其分配适当的资源。即插即用也需要芯片组的支持。