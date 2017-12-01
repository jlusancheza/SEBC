# Teragen
```
[saturn@ip-10-0-3-219 centos]$ time hadoop jar /opt/cloudera/parcels/CDH/jars/hadze=32m  -Dmapreduce.map.memory.mb=512 65536000  /user/saturn/tgen
17/12/01 19:16:01 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-3
17/12/01 19:16:02 INFO terasort.TeraSort: Generating 65536000 using 12
17/12/01 19:16:02 INFO mapreduce.JobSubmitter: number of splits:12
17/12/01 19:16:02 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_151
17/12/01 19:16:03 INFO impl.YarnClientImpl: Submitted application application_151
17/12/01 19:16:03 INFO mapreduce.Job: The url to track the job: http://ip-10-0-3-
17/12/01 19:16:03 INFO mapreduce.Job: Running job: job_1512153918383_0001
17/12/01 19:16:09 INFO mapreduce.Job: Job job_1512153918383_0001 running in uber
17/12/01 19:16:09 INFO mapreduce.Job:  map 0% reduce 0%
17/12/01 19:16:20 INFO mapreduce.Job:  map 9% reduce 0%
17/12/01 19:16:23 INFO mapreduce.Job:  map 18% reduce 0%
17/12/01 19:16:24 INFO mapreduce.Job:  map 24% reduce 0%
17/12/01 19:16:26 INFO mapreduce.Job:  map 29% reduce 0%
17/12/01 19:16:27 INFO mapreduce.Job:  map 33% reduce 0%
17/12/01 19:16:30 INFO mapreduce.Job:  map 39% reduce 0%
17/12/01 19:16:31 INFO mapreduce.Job:  map 41% reduce 0%
17/12/01 19:16:33 INFO mapreduce.Job:  map 44% reduce 0%
17/12/01 19:16:34 INFO mapreduce.Job:  map 45% reduce 0%
17/12/01 19:16:36 INFO mapreduce.Job:  map 48% reduce 0%
17/12/01 19:16:38 INFO mapreduce.Job:  map 49% reduce 0%
17/12/01 19:16:39 INFO mapreduce.Job:  map 52% reduce 0%
17/12/01 19:16:42 INFO mapreduce.Job:  map 55% reduce 0%
17/12/01 19:16:44 INFO mapreduce.Job:  map 57% reduce 0%
17/12/01 19:16:45 INFO mapreduce.Job:  map 59% reduce 0%
17/12/01 19:16:47 INFO mapreduce.Job:  map 61% reduce 0%
17/12/01 19:16:48 INFO mapreduce.Job:  map 63% reduce 0%
17/12/01 19:16:50 INFO mapreduce.Job:  map 65% reduce 0%
17/12/01 19:16:52 INFO mapreduce.Job:  map 67% reduce 0%
17/12/01 19:16:54 INFO mapreduce.Job:  map 68% reduce 0%
17/12/01 19:16:55 INFO mapreduce.Job:  map 70% reduce 0%
17/12/01 19:16:57 INFO mapreduce.Job:  map 72% reduce 0%
17/12/01 19:16:58 INFO mapreduce.Job:  map 73% reduce 0%
17/12/01 19:17:00 INFO mapreduce.Job:  map 75% reduce 0%
17/12/01 19:17:01 INFO mapreduce.Job:  map 76% reduce 0%
17/12/01 19:17:03 INFO mapreduce.Job:  map 78% reduce 0%
17/12/01 19:17:04 INFO mapreduce.Job:  map 80% reduce 0%
17/12/01 19:17:06 INFO mapreduce.Job:  map 82% reduce 0%
17/12/01 19:17:07 INFO mapreduce.Job:  map 83% reduce 0%
17/12/01 19:17:09 INFO mapreduce.Job:  map 85% reduce 0%
17/12/01 19:17:10 INFO mapreduce.Job:  map 87% reduce 0%
17/12/01 19:17:12 INFO mapreduce.Job:  map 89% reduce 0%
17/12/01 19:17:13 INFO mapreduce.Job:  map 90% reduce 0%
17/12/01 19:17:15 INFO mapreduce.Job:  map 93% reduce 0%
17/12/01 19:17:16 INFO mapreduce.Job:  map 94% reduce 0%
17/12/01 19:17:18 INFO mapreduce.Job:  map 96% reduce 0%
17/12/01 19:17:19 INFO mapreduce.Job:  map 97% reduce 0%
17/12/01 19:17:20 INFO mapreduce.Job:  map 98% reduce 0%
17/12/01 19:17:21 INFO mapreduce.Job:  map 99% reduce 0%
17/12/01 19:17:22 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 19:17:24 INFO mapreduce.Job: Job job_1512153918383_0001 completed succes
17/12/01 19:17:25 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1469594
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=1025
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=48
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=24
        Job Counters
                Launched map tasks=12
                Other local map tasks=12
                Total time spent by all maps in occupied slots (ms)=763431
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=763431
                Total vcore-seconds taken by all map tasks=763431
                Total megabyte-seconds taken by all map tasks=781753344
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=1025
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=2460
                CPU time spent (ms)=148190
                Physical memory (bytes) snapshot=2465689600
                Virtual memory (bytes) snapshot=13611798528
                Total committed heap usage (bytes)=4465885184
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    1m25.334s
user    0m5.008s
sys     0m0.301s
```
## Command hdfs dfs -ls /user/saturn/tgen
```
[saturn@ip-10-0-3-219 centos]$ hdfs dfs -ls /user/saturn/tgen
Found 13 items
-rw-r--r--   3 saturn planets          0 2017-12-01 19:17 /user/saturn/tgen/_SUCCESS
-rw-r--r--   3 saturn planets  546133400 2017-12-01 19:16 /user/saturn/tgen/part-m-00000
-rw-r--r--   3 saturn planets  546133300 2017-12-01 19:16 /user/saturn/tgen/part-m-00001
-rw-r--r--   3 saturn planets  546133300 2017-12-01 19:17 /user/saturn/tgen/part-m-00002
-rw-r--r--   3 saturn planets  546133400 2017-12-01 19:17 /user/saturn/tgen/part-m-00003
-rw-r--r--   3 saturn planets  546133300 2017-12-01 19:17 /user/saturn/tgen/part-m-00004
-rw-r--r--   3 saturn planets  546133300 2017-12-01 19:17 /user/saturn/tgen/part-m-00005
-rw-r--r--   3 saturn planets  546133400 2017-12-01 19:17 /user/saturn/tgen/part-m-00006
-rw-r--r--   3 saturn planets  546133300 2017-12-01 19:17 /user/saturn/tgen/part-m-00007
-rw-r--r--   3 saturn planets  546133300 2017-12-01 19:17 /user/saturn/tgen/part-m-00008
-rw-r--r--   3 saturn planets  546133400 2017-12-01 19:17 /user/saturn/tgen/part-m-00009
-rw-r--r--   3 saturn planets  546133300 2017-12-01 19:17 /user/saturn/tgen/part-m-00010
-rw-r--r--   3 saturn planets  546133300 2017-12-01 19:17 /user/saturn/tgen/part-m-00011

```


## Blocks fsck
```
[saturn@ip-10-0-3-219 centos]$ hdfs fsck -blocks /user/saturn
Connecting to namenode via http://ip-10-0-3-17.ec2.internal:50070
FSCK started by saturn (auth:SIMPLE) from /10.0.3.219 for path /user/saturn at Fri Dec 01 19:20:21 UTC 2017
.............Status: HEALTHY
 Total size:    6553600000 B
 Total dirs:    3
 Total files:   13
 Total symlinks:                0
 Total blocks (validated):      204 (avg. block size 32125490 B)
 Minimally replicated blocks:   204 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Fri Dec 01 19:20:21 UTC 2017 in 10 milliseconds


The filesystem under path '/user/saturn' is HEALTHY

```