# 固定实时任务和软实时任务的区别

> 原文:[https://www . geesforgeks . org/公司实时任务和软实时任务的区别/](https://www.geeksforgeeks.org/difference-between-firm-real-time-tasks-and-soft-real-time-tasks/)

实时任务通常分为硬任务和软任务，但在很大范围内，实时任务分为:

1.  硬实时任务
2.  固定实时任务
3.  软实时任务

**1。公司实时任务:**
公司实时任务是这样一种类型的实时任务，它与时间限制相关联，并且任务需要在截止日期内产生结果。虽然固定实时任务不同于硬实时任务，因为一旦过了期限，任务没有完成，系统就会失败，但是如果是固定实时任务，即使过了期限，系统也不会失败。

**示例:**

```
1. Video conferencing
2. Satellite based tracking 
```

**2。软实时任务:**
软实时任务是这样一种类型的实时任务，它也与时间限制相关联，但是在这里时间限制并不表示为绝对值。在软实时任务中，即使在截止日期之后，结果也不会被认为是不正确的，也不会发生系统故障。

**示例:**

```
1. Web browsing
2. Railway Ticket Reservation 
```

**硬实时任务和软实时任务的区别:**

<center>

| 坚定的实时任务 | 软实时任务 |
| --- | --- |
| 它需要在期限内完成。 | 它也需要在期限内完成，但不严格。 |
| 相关定时约束的值被认为是绝对的。 | 相关定时约束的值作为平均值。 |
| 截止日期后，结果的效用为零。 | 截止日期后，结果的效用降低，但逐渐变为零。 |
| 截止日期后获得的结果被认为是不正确的。 | 截止日期后获得的结果没有错误。 |
| 它被广泛应用于多媒体应用中。 | 它在这类应用中使用较少。 |
| 在实际应用中使用较少。 | 在实际应用中得到广泛应用。 |
| 例子:基于卫星的跟踪。 | 例子:火车票预订。 |

</center>