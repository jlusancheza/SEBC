# Kerberos Test

```
[centos@ip-10-0-3-79 ~]$ kinit jlusancheza
Password for jlusancheza@EC2.INTERNAL:
[centos@ip-10-0-3-79 ~]$ hdfs dfs -ls /user/jlusancheza
Found 7 items
drwx------   - jlusancheza jlusancheza          0 2017-11-29 17:00 /user/jlusancheza/.Trash
drwx------   - jlusancheza jlusancheza          0 2017-11-28 22:19 /user/jlusancheza/.staging
drwxr-xr-x   - jlusancheza jlusancheza          0 2017-11-28 22:19 /user/jlusancheza/results
drwxr-xr-x   - jlusancheza jlusancheza          0 2017-11-28 17:03 /user/jlusancheza/teragen
drwxr-xr-x   - jlusancheza jlusancheza          0 2017-11-28 17:03 /user/jlusancheza/teragen-10Gb
drwxr-xr-x   - jlusancheza jlusancheza          0 2017-11-28 17:12 /user/jlusancheza/terasort-10Gb
-rw-r--r--   3 jlusancheza jlusancheza    2505716 2017-11-29 16:33 /user/jlusancheza/training.sql
[centos@ip-10-0-3-79 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_500
Default principal: jlusancheza@EC2.INTERNAL

Valid starting     Expires            Service principal
11/29/17 18:03:40  11/30/17 18:03:40  krbtgt/EC2.INTERNAL@EC2.INTERNAL
        renew until 12/06/17 18:03:40


```