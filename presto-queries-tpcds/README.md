These are the full 99 TPC-DS queries from Presto.

- https://github.com/prestosql/presto/tree/master/presto-benchto-benchmarks/src/main/resources/sql/presto/tpcds

修改部分
========

- q05.sql、q16.sql、q21.sql、q30.sql、q32.sql、q72.sql、q77.sql、q83.sql、q92.sql、q94.sql

语法报错例如：LINE 8: AND ("d_date" BETWEEN CAST('2000-01-27' AS DATE) AND (CAST('2000-01-27' AS DATE) + INTERVAL '90' DAY))
修改：d_date修改为CAST("d_date" AS DATE)

- q58:

语法报错：LINE 19: WHERE ("d_date" = CAST('2000-01-03' AS DATE))
修改：WHERE ("d_date" = '2000-01-03' )

- q64:

增加 LIMIT 100,避免结果集太多

- q30.sql 

字段错误：c_last_review_date_sk 修改为c_last_review_date



