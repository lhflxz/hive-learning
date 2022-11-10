# hive-learning
hive学习记录



with cube



lateral view explode



regexp_replace



日期函数、月初月末本周上周

```hive
TRUNC('${f_date}','MM') -- 当月第一天

LAST_DAY('${f_date}') -- 当月最后一天

date_sub('${f_date}', weekday(cast('${f_date} 00:00:00' as DATETIME))) -- 本周的第一天，周一

date_sub('${f_date}',weekday(cast('${f_date} 00:00:00' as DATETIME))-6) -- 本周的最后一天，周日
```



参数，mapjoin



bitmap位图思想应用

