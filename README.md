# bigdataMonitor
通过cloudera manager/ResourceManager/Flink API来监控相应应用的状态并输出json给splunk


# 介绍

yarn_app_monit.py： 通过ResourceManager的API来监控应用状态

monit.py： 通过Cloudera Manager的API来监控组件状态

flink_monitor.py： 通过flink的API来监控运行的流式程序的状态

outbox_monitor.py:  连接mysql/oracle/hive查询相关元数据监控业务状态

addmysql_partition.py：  定时增加第二天的mysql分区

oracle.py：  连接oracle的类

mysql4partition.py： 连接mysql的类

当然还有i连接kerberos认证的hive的函数，见outbox_monitor.py

# crontab

*/10 * * * * /bigf/admin/monitor/run_monit.sh


