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

```hive
FAILED: ODPS-0010000:System internal error - fuxi job failed, caused by: Hash Join Cursor HashJoin4#0 small table exceeds, memory limit(MB) 640, fixed memory used 596533248, string memory used 74566656, complex type memory used 0

set odps.sql.mapjoin.memory.max=2000;
```



bitmap位图思想应用

