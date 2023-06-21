# 多用途互联网邮件扩展协议

> 原文:[https://www . geesforgeks . org/多用-互联网-邮件-扩展名-mime-protocol/](https://www.geeksforgeeks.org/multipurpose-internet-mail-extension-mime-protocol/)

**多用途互联网邮件扩展(MIME)** 是 Bell Communications 在 1991 年提出的标准，旨在扩展电子邮件的有限功能。
MIME 是一种附加协议*或补充协议*，允许通过 SMTP 发送非 ASCII 数据。它允许用户在互联网上交换不同种类的数据文件:音频、视频、图像以及应用程序。

**我们为什么需要 MIME？**
简单邮件传输协议(SMTP)的局限性:

1.  SMTP 的结构非常简单
2.  然而，它的简单是有代价的，因为它只发送 NVT 7 位 ASCII 格式的消息。
3.  它不能用于不支持 7 位 ASCII 格式的语言，如法语、德语、俄语、汉语和日语等。所以不能用 SMTP 传输。所以，为了让 SMTP 更广泛，我们使用了 MIME。
4.  它不能用于发送二进制文件或视频或音频数据。

**MIME 的目的和功能–**
随着人们也想用多媒体表达自己，对电子邮件的需求越来越大。因此，引入了另一个 MIME 电子邮件应用程序，因为它不限于文本数据。

MIME *将发送端的非 ASCII 数据*转换为 NVT 7 位数据，并将其传送到客户端 SMTP。接收端的消息被传输回原始数据。此外，我们可以使用 MIME 发送视频和音频数据，因为它也以 7 位 ASCII 数据传输它们。

**哑剧的特点–**

1.  它能够用一封邮件发送多个附件。
2.  无限消息长度。
3.  如果需要，可以分割二进制附件(可执行文件、图像、音频或视频文件)。
4.  MIME 为不同的内容类型和多部分消息提供了支持。

**MIME 的工作方式–**
假设用户想通过用户代理发送一封电子邮件，而这封邮件是非 ASCII 格式的，因此有一个 MIME 协议可以将其转换为 7 位 NVT ASCII 格式。消息通过电子邮件系统以 7 位格式传输到另一方。现在，MIME 协议再次将其转换回非 ASCII 代码，现在，接收方的用户代理读取它，然后信息最终由接收方读取。MIME 标头基本上是在任何电子邮件传输的开头插入的。

**使用 SMTP 和 POP 的 MIME–**
SMTP 将作为邮件传输代理的邮件从发送方传输到接收方的邮箱并存储，MIME 标头添加到原始标头并提供附加信息。而 POP 是消息访问代理，它将邮件从邮件服务器组织到接收者的计算机。POP 允许用户代理与消息传输代理连接。

**MIME 标头:**
它被添加到原始电子邮件标头部分以定义转换。我们在原标题上增加了*五个标题*:

1.  **MIME-Version–**定义 MIME 协议的版本。它必须具有参数*值 1.0* ，这表明消息是使用 MIME 格式化的。
2.  **内容类型–**消息正文中使用的数据类型。它们有不同的类型，如文本数据(纯文本、HTML)、音频内容或视频内容。
3.  **内容类型编码–**它定义了用于编码消息的方法。比如 7 位编码、8 位编码等。
4.  **内容标识–**用于唯一标识消息。
5.  **内容描述–**定义身体实际上是图像、视频还是音频。