These are the full 99 TPC-DS queries from Apache Spark 2.2.

- https://github.com/apache/spark/tree/master/sql/core/src/test/resources/tpcds

问题
========

* Hive:
- q24

Hive 跑不过去，建议使用 https://github.com/hortonworks/hive-testbench/blob/hdp3/sample-queries-tpcds/query24.sql

- q53:

```
8 moreCaused by: java.lang.NullPointerException at org.apache.hadoop.hive.ql.exec.persistence.PTFRowContainer.first(PTFRowContainer.java:115) at org.apache.hadoop.hive.ql.exec.PTFPartition.iterator(PTFPartition.java:114) 
```

[Hive-18786](https://issues.apache.org/jira/browse/HIVE-18786)

- q64

增加 LIMIT 100

- q72 

Hive 时间很长

* Spark:

Spark 部分语句跑不了，需要设置：
spark.sql.crossJoin.enabled=true

