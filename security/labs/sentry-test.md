```
[jlusancheza@ip-10-0-3-79 centos]$ kinit jlusancheza
Password for jlusancheza@EC2.INTERNAL:
[jlusancheza@ip-10-0-3-79 centos]$ beeline
Beeline version 1.1.0-cdh5.12.1 by Apache Hive
beeline>  !connect jdbc:hive2://10.0.3.79:10000/default;principal=hive/ip-10-0-3-
scan complete in 2ms
Connecting to jdbc:hive2://10.0.3.79:10000/default;principal=hive/ip-10-0-3-79.ec
Connected to: Apache Hive (version 1.1.0-cdh5.12.1)
Driver: Hive JDBC (version 1.1.0-cdh5.12.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://10.0.3.79:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20171129184040_d5c2b375-4223-4c68-910a-78a
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, ty
INFO  : Completed compiling command(queryId=hive_20171129184040_d5c2b375-4223-4c6
INFO  : Executing command(queryId=hive_20171129184040_d5c2b375-4223-4c68-910a-78a
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171129184040_d5c2b375-4223-4c6
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (0.34 seconds)




[centos@ip-10-0-3-79 ~]$ kinit george
Password for george@EC2.INTERNAL:
[centos@ip-10-0-3-79 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_500
Default principal: george@EC2.INTERNAL

Valid starting     Expires            Service principal
11/29/17 19:23:58  11/30/17 19:23:58  krbtgt/EC2.INTERNAL@EC2.INTERNAL
        renew until 12/06/17 19:23:58
[centos@ip-10-0-3-79 ~]$ beeline
Beeline version 1.1.0-cdh5.12.1 by Apache Hive
beeline> !connect jdbc:hive2://10.0.3.79:10000/default;principal=hive/ip-10-0-3-79.ec2.internal@EC2.INTERNAL
scan complete in 1ms
Connecting to jdbc:hive2://10.0.3.79:10000/default;principal=hive/ip-10-0-3-79.ec2.internal@EC2.INTERNAL
Connected to: Apache Hive (version 1.1.0-cdh5.12.1)
Driver: Hive JDBC (version 1.1.0-cdh5.12.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://10.0.3.79:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20171129192525_be2728d3-7a78-40d9-8923-a0b214be4fcc): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171129192525_be2728d3-7a78-40d9-8923-a0b214be4fcc); Time taken: 0.075 seconds
INFO  : Executing command(queryId=hive_20171129192525_be2728d3-7a78-40d9-8923-a0b214be4fcc): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171129192525_be2728d3-7a78-40d9-8923-a0b214be4fcc); Time taken: 0.137 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
| ubigeo    |
| ventas    |
+-----------+--+
2 rows selected (0.319 seconds)
0: jdbc:hive2://10.0.3.79:10000/default> !q
Closing: 0: jdbc:hive2://10.0.3.79:10000/default;principal=hive/ip-10-0-3-79.ec2.internal@EC2.INTERNAL



[centos@ip-10-0-3-79 ~]$ kinit ferdinand
Password for ferdinand@EC2.INTERNAL:
[centos@ip-10-0-3-79 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_500
Default principal: ferdinand@EC2.INTERNAL

Valid starting     Expires            Service principal
11/29/17 19:25:48  11/30/17 19:25:48  krbtgt/EC2.INTERNAL@EC2.INTERNAL
        renew until 12/06/17 19:25:48
[centos@ip-10-0-3-79 ~]$ beeline
Beeline version 1.1.0-cdh5.12.1 by Apache Hive
beeline> !connect jdbc:hive2://10.0.3.79:10000/default;principal=hive/ip-10-0-3-79.ec2.internal@EC2.INTERNAL
scan complete in 2ms
Connecting to jdbc:hive2://10.0.3.79:10000/default;principal=hive/ip-10-0-3-79.ec2.internal@EC2.INTERNAL
Connected to: Apache Hive (version 1.1.0-cdh5.12.1)
Driver: Hive JDBC (version 1.1.0-cdh5.12.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://10.0.3.79:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20171129192727_65cf78a0-3caa-40d0-9971-e0a327291e92): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171129192727_65cf78a0-3caa-40d0-9971-e0a327291e92); Time taken: 0.074 seconds
INFO  : Executing command(queryId=hive_20171129192727_65cf78a0-3caa-40d0-9971-e0a327291e92): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171129192727_65cf78a0-3caa-40d0-9971-e0a327291e92); Time taken: 0.136 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
| ubigeo    |
+-----------+--+
1 row selected (0.334 seconds)

```
