# 网络模拟器 3

> 原文:[https://www.geeksforgeeks.org/network-simulator-3/](https://www.geeksforgeeks.org/network-simulator-3/)

**网络模拟器**是通过用 C++或 Python 编写脚本，在一台计算机上模拟真实世界网络的工具。通常如果我们想进行实验，看看我们的网络如何使用各种参数工作。我们没有制造不同拓扑所需的计算机和路由器数量。即使我们有这些资源，为实验目的建立这样一个网络也是非常昂贵的。

因此，为了克服这些缺点，我们使用了 NS3，这是一个用于互联网的离散事件网络模拟器。NS3 有助于创建各种虚拟节点(即现实生活中的计算机)，在各种 Helper 类的帮助下，它允许我们在节点上安装设备、互联网堆栈、应用程序等。

使用 NS3，我们可以在节点之间创建点对点、无线、CSMA 等连接。点对点连接与两台计算机之间连接的局域网相同。无线连接与各种电脑和路由器之间的 WiFi 连接相同。CSMA 连接与计算机之间的总线拓扑相同。建立连接后，我们尝试在每个节点上安装网卡，以实现网络连接。

当设备中启用网卡时，我们会在通道(即用于发送数据的真实路径)中添加不同的参数，如数据速率、数据包大小等。现在，我们使用应用程序生成流量，并使用这些应用程序发送数据包。

Ns3 为我们提供了可用于现实生活集成的特殊功能。其中一些功能是:

1.  **追踪节点:**
    NS3 允许我们追踪节点的路由，这有助于我们知道发送或接收了多少数据。生成跟踪文件来监控这些活动。
2.  **NetAnim:**
    它代表网络动画师。这是一个动画版本，展示了网络的真实情况以及数据如何从一个节点传输到另一个节点。
3.  **Pcap 文件:**
    NS3 帮助生成 Pcap 文件，可用于获取数据包的所有信息(如序列号、源 IP、目的 IP 等)。这些 pcaps 可以通过一个叫做 wireshark 的软件工具看到。
4.  **gnuPlot:**
    GnuPlot 用于根据我们从 NS3 的跟踪文件中获得的数据绘制图表。与其他图形制作工具相比，Gnuplot 提供了更精确的图形，而且它比其他工具更简单。

这是对 NS3 的简单介绍。基本上，NS3 可以执行现实中网络中执行的大多数活动。