# RC5 加密算法

> 原文:[https://www.geeksforgeeks.org/rc5-encryption-algorithm/](https://www.geeksforgeeks.org/rc5-encryption-algorithm/)

RC5 是 Ron Rivest 于 1994 年设计的对称密钥块加密算法。值得注意的是它简单、快速(因为只使用了像异或、移位等基本的计算机运算。)并且消耗更少的内存。

**示例:**

```
Key : 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
Plain Text : 00000000 00000000
Cipher Text : EEDBA521 6D8F4B15

```

RC5 是一种分组密码，一次寻址两个字块。
根据输入的纯文本块大小、轮数和密钥大小，可以定义 RC5 的各种实例，并将每个实例表示为 RC5-w/r/b，其中 w =以比特为单位的字大小，r =轮数，b =以字节为单位的密钥大小。
允许值为:

<center>

| 参数 | 可能值 |
| --- | --- |
| 块/字大小(位) | 16, 32, 64 |
| 回合数 | 0 – 255 |
| 密钥大小(字节) | 0 – 255 |

**注意–**由于 RC5 一次使用 2 个字块，纯文本块大小可以是 32、64 或 128 位。

算法中使用的符号:

<center>

| 标志 | 操作 |
| --- | --- |
| x <<< y | x 按 y 位循环左移 |
| + | 以![2^w](img/1c842cf944e8c033349730576acd7697.png "Rendered by QuickLaTeX.com")为模的二进制补码加法 |
| ^ | 按位异或 |

</center>

**步骤-1:** 常数 P 和 Q 的初始化。
RC5 利用 2 个神奇的常数 P 和 Q，其值由字长 w 定义

<center>

| 字长(位) | P（十六进制） | Q（十六进制） |
| --- | --- | --- |
| Sixteen | b7e1 | 9e37 |
| Thirty-two | b7e15163 | 9e3779b9 |
| Sixty-four | B7 和 151628 aed 2 至 6b | 9e3779b97f4a7c15 |

</center>

对于任何其他字长，P 和 Q 可以确定为:

```
P = Odd((e-2)) 
Q = Odd((-2))

```

这里，奇数(x)是最接近 x 的奇数整数，e 是自然对数的基数，![\phi](img/2e8a7ac66542317be45c695ae849580d.png "Rendered by QuickLaTeX.com")是黄金分割比。

**步骤-2:** 将密钥 K 从字节转换为字。
大小为 b 字节的密钥 K 用于初始化由 c 个字组成的数组 L，其中 c = b/u，u = w/8，w =用于 RC5 特定实例的字大小。例如，如果我们选择 w=32 位，密钥 k 的大小为 96 字节，那么 u=32/8=4，c=b/u=96/4=24。
在向 L 添加密钥 K 之前，L 被预初始化为 0 值。

```
for i=b-1 to 0
    L[i/u] = (L[u/i] <<< 8) + K[i]

```

**步骤-3:** 初始化子密钥 S。
大小为 t=2(r+1)的子密钥 S 使用魔法常数 P 和 q 初始化

```
S[0] = P
for i = 1 to 2(r+1)-1
    S[i] = S[i-1] + Q)

```

**第 4 步:**子键混合。
RC5 加密算法使用子密钥 S. L .仅仅是，基于用户输入的密钥形成的临时数组。
用 S 和 l 混合输入用户的密钥

```
i = j = 0
A = B = 0
do 3 * max(t, c) times:
    A = S[i] = (S[i] + A + B) <<< 3
    B = L[j] = (L[j] + A + B) <<< (A + B)
    i = (i + 1) % t
    j = (j + 1) % c

```

**第 5 步:**加密。
我们将输入的纯文本块分成大小为 w 位的两个寄存器 A 和 B。在经历加密过程之后，A 和 B 的结果一起形成密文块。
RC5 加密算法:

1.  通过将 S[0]和 S[1]分别添加到 A 和 B，对纯文本块 A 和 B 进行一次性初始化。这些操作很简单。
2.  异或 a 和 B. A=A^B
3.  将 A 的新值向左循环移位 B 位。
4.  将 S[2*i]添加到上一步的输出中。这是 a 的新价值。
5.  将 B 与 A 的新值进行异或运算，并存储在 B 中
6.  将 B 的新值向左循环移位 A 位。
7.  将 S[2*i+1]添加到上一步的输出中。这就是 b 的新价值。
8.  重复整个过程(除了一次初始化)r 次。

```
A = A + S[0] 
B = B + S[1]
for i = 1 to r do:
    A = ((A ^ B) <<< B) + S[2 * i]
    B = ((B ^ A) <<< A) + S[2 * i + 1]
return A, B

```

或者，RC5 解密可以定义为:

```
for i = r down to 1 do:
    B = ((B - S[2 * i + 1]) >>> A) ^ A
    A = ((A - S[2 * i]) >>> B) ^ B
B = B - S[1]
A = A - S[0]
return A, B

```

</center>