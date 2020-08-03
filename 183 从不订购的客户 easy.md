<img src = 'https://github.com/leopardv10/MySQL/blob/master/images/183.1.png?raw=true' width = 50%>

<img src = 'https://github.com/leopardv10/MySQL/blob/master/images/183.2.png?raw=true' width = 50%>

### 题解：

```sql
# Write your MySQL query statement below
select a.Name as Customers 
from Customers a left join Orders b on a.Id = b.CustomerId
where CustomerId is null;

# left join 连接两表后，orders表中会有一部分CutomerId的值为null
# 没有下单的顾客对应的CustomerId即为null
# 两个表连接条件用on
```

