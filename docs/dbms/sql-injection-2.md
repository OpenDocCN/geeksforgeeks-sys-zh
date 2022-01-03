# SQL 注入

> 原文:[https://www.geeksforgeeks.org/sql-injection-2/](https://www.geeksforgeeks.org/sql-injection-2/)

SQL 注入是一种通过将 SQL 命令作为语句注入网页输入来利用用户数据的技术。基本上，这些语句可以被恶意用户用来操纵应用程序的 web 服务器。

*   SQL 注入是一种代码注入技术，可能会破坏您的数据库。
*   SQL 注入是最常见的网络黑客技术之一。
*   SQL 注入是通过网页输入在 SQL 语句中放置恶意代码。

**<font size="3" color="Black">在网络应用中开发 SQL 注入</font>**

Web 服务器在需要检索或存储用户数据的任何时候都可以与数据库服务器通信。攻击者设计的 SQL 语句可以在 web 服务器从应用服务器获取内容时执行。它损害了 web 应用程序的安全性。

**SQL 注入示例**
假设我们有一个基于学生记录的应用程序。通过输入唯一的私人学生证，任何学生只能查看自己的记录。假设我们有一个如下所示的字段:
**学号:**

学生在输入栏中输入以下内容:
**12222345 或 1=1** 。

所以这个基本上**翻译成:**

```
SELECT * from STUDENT where 
STUDENT-ID == 12222345 or 1 = 1
```

现在这个 **1=1** 将返回所有适用的记录。所以基本上，所有的学生数据都被泄露了。现在，恶意用户也可以以类似的方式删除学生记录。

考虑下面的 SQL 查询。

```
SELECT * from USER where 
USERNAME = “” and PASSWORD=”” 
```

现在，恶意者可以聪明地使用“=”操作符来检索私有和安全的用户信息。因此，执行以下查询时，不是上述查询，而是检索受保护的数据，而不是显示给用户。

```
Select * from User where 
(Username = “” or 1=1) AND 
(Password=”” or 1=1).
```

由于 **1=1** 始终成立，用户数据被泄露。

**SQL 注入的影响**
黑客可以检索数据库中存在的所有用户数据，如用户详细信息、信用卡信息、社会安全号码，还可以访问管理员门户等受保护区域。也可以从表中删除用户数据。
如今，所有的网购应用、银行交易都使用后端数据库服务器。因此，万一黑客能够利用 SQL 注入，整个服务器都会受到威胁。

**防止 SQL 注入**

*   用户验证:通过预定义输入字段的长度、输入类型和验证用户来验证用户的输入。
*   限制用户的访问权限，并定义任何外部人员可以从数据库访问的数据量。基本上，不应该授予用户访问数据库中所有内容的权限。
*   不要使用系统管理员帐户。

[基本 SQL 注入和缓解示例](https://www.geeksforgeeks.org/basic-sql-injection-mitigation-example/)