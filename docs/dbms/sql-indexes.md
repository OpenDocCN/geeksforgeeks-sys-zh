# SQL 索引

> 原文:[https://www.geeksforgeeks.org/sql-indexes/](https://www.geeksforgeeks.org/sql-indexes/)

索引是一个模式对象。服务器使用它通过使用指针来加速行的检索。通过使用快速路径访问方法快速定位数据，可以减少磁盘输入输出。索引有助于加快选择查询和 where 子句的速度，但它会降低数据输入的速度，例如 update 和 insert 语句。可以在不影响数据的情况下创建或删除索引。在本文中，我们将看到如何在数据库中创建、删除和使用 INDEX。

例如，如果您想引用某本书中讨论某个主题的所有页面，则首先要引用索引，该索引按字母顺序列出所有主题，然后引用一个或多个特定的页码。

### **创建索引:**

**语法:**

```
 CREATE INDEX index
 ON TABLE column;
```

其中**索引**是该索引的名称，**表**是在其上创建该索引的表的名称，**列**是该索引所应用的列的名称。

### **多列:**

**语法:**

```
 CREATE INDEX index
 ON TABLE (column1, column2,.....);
```

### **独特指数:**

唯一索引用于维护表中数据的完整性以及快速性能，它不允许多个值输入表中。
**语法:**

```
CREATE UNIQUE INDEX index
 ON TABLE column;
```

### **何时应该创建索引:**

*   一列包含多种值。
*   列不包含大量空值。
*   在 where 子句或联接条件中，一列或多列经常一起使用。

### 

**什么时候应该避开指数:**

*   这张桌子很小
*   列不经常在查询中用作条件
*   该列经常更新

### 

**删除索引:**

使用**删除索引**命令从数据字典中删除索引。

**语法:**

```
DROP INDEX index;
```

要删除一个索引，您必须是该索引的所有者或拥有**删除任何索引**特权。

### **改变指数:**

通过重建或重新组织索引来修改现有表的索引。

```
ALTER INDEX IndexName 
ON TableName REBUILD;
```

### **确认指标:**

您可以检查用户或服务器本身给定的特定表中存在的不同索引及其唯一性。

**语法:**

```
select * from USER_INDEXES;
```

它将向您显示服务器中存在的所有索引，您也可以在其中找到自己的表。

### **重命名索引:**

可以使用系统存储过程 sp_rename 来重命名数据库中的任意索引。

**语法:**

```
EXEC sp_rename  
   index_name,  
   new_index_name,  
   N'INDEX'; 
```