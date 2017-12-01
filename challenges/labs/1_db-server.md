# DB Server
```
[centos@ip-10-0-3-120 ~]$ hostname -f
ip-10-0-3-120.ec2.internal
[centos@ip-10-0-3-120 ~]$ mysql --version
mysql  Ver 14.14 Distrib 5.7.20, for Linux (x86_64) using  EditLine wrapper
[centos@ip-10-0-3-120 ~]$ mysql -u root -p
Enter password:
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 5
Server version: 5.7.20 MySQL Community Server (GPL)

Copyright (c) 2000, 2017, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sys                |
+--------------------+
9 rows in set (0.00 sec)

```