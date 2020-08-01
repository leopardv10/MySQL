<img src = 'https://github.com/leopardv10/MySQL/blob/master/images/182.png?raw=true' width = 50%>

### 解法一：创建辅助表

```SQL
# Write your MySQL query statement below
select Email from  # 从辅助表中选择Email
(select Email, count(Email) as c from Person group by Email) as helper  # helper即为辅助表
where c > 1;  # 限制条件是Email对应的c > 1
```

### 解法二：

```sql
select Email from Person
group by Email  # 以Email为类别汇总Person表
having count(Email) > 1;  # 注意where不能与count连用，必须使用having
```

