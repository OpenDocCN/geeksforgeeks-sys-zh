# 物联网中的无线媒体接入问题

> 原文:[https://www . geesforgeks . org/无线媒体接入物联网问题/](https://www.geeksforgeeks.org/wireless-media-access-issues-in-internet-of-things/)

当涉及到使用无线介质的通信时，总是担心由于其他现有无线通信技术而产生的干扰。无线是指不使用物理介质(即电线)的通信和信息传输。

让我们了解他们之间是如何沟通的。不同的移动站连接到发射机/接收机，由其他节点通过共享信道进行通信。在这种类型的通信中，它使媒体访问控制设计比有线网络更困难。

观察到的非常重要的问题是:半双工操作、时变信道和突发信道错误。
这些解释如下。

**1。半双工操作:**
半双工传输是指发送方和接收方都能够共享数据，但一次只能共享一个数据。在无线传输中，当发射机发送数据时，很难接收数据，因为在传输过程中，广播时会泄漏大量或大部分信号能量。传输信号和接收信号的幅度相差很大。因此，由于传输信号的强度大于接收信号的强度，发送方甚至不可能进行冲突检测。因此，这导致了碰撞问题，首要重点应该是尽量减少碰撞

**2。时变信道:**
时变信道包括无线电信号传播的三种机制:反射、衍射和散射。

*   **反射–**
    当携带信息的传播波侵入一个比波的波长大得多的物体时，就会发生这种情况。
*   **衍射–**
    当发射器和接收器之间的无线电路径被具有尖锐边缘的表面碰撞时，就会出现这种情况。这是导致波从目标位置衍射的现象。
*   **散射–**
    当波传播的介质由一些尺寸小于波的波长的物体组成时，就会出现这种情况。

当节点传输信号时，这些信号是时移的，这被称为多径传播。而当该节点的信号强度下降到阈值以下时，这被称为衰落。因此，握手策略被广泛使用，以便建立健康的通信。

**3。突发信道错误:**
突发信道错误被称为在通信信道中接收的连续符号序列，其中第一个和最后一个符号有错误，并且没有证据表明已校正的接收符号的连续子序列。当使用时变信道时，会引入信号强度，从而在传输中观察到误差。对于有线网络中的这些信道，比特率高达 10 <sup>-3</sup> 。