# HDFS testing

## Test HDFS throughput - Teragen/Terasort

### Teragen
```

[jlusancheza@ip-10-0-3-126 centos]$  time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-m                                                                                                    apreduce-examples-2.6.0-cdh5.12.1.jar  teragen -Dmapreduce.job.maps=4 -Ddfs.blocksize=32m  1                                                                                                    00000000 /user/jlusancheza/teragen-10Gb
17/11/28 16:59:13 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-3-126.ec2.in                                                                                                    ternal/10.0.3.126:8032
17/11/28 16:59:14 INFO terasort.TeraGen: Generating 100000000 using 4
17/11/28 16:59:14 INFO mapreduce.JobSubmitter: number of splits:4
17/11/28 16:59:15 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1511823443481_0002
17/11/28 16:59:16 INFO impl.YarnClientImpl: Submitted application application_1511823443481_0002
17/11/28 16:59:16 INFO mapreduce.Job: The url to track the job: http://ip-10-0-3-126.ec2.internal:8088/proxy/application_1511823443481_0002/
17/11/28 16:59:16 INFO mapreduce.Job: Running job: job_1511823443481_0002
17/11/28 16:59:27 INFO mapreduce.Job: Job job_1511823443481_0002 running in uber mode : false
17/11/28 16:59:27 INFO mapreduce.Job:  map 0% reduce 0%
17/11/28 16:59:47 INFO mapreduce.Job:  map 4% reduce 0%
17/11/28 16:59:53 INFO mapreduce.Job:  map 6% reduce 0%
17/11/28 16:59:59 INFO mapreduce.Job:  map 7% reduce 0%
17/11/28 17:00:05 INFO mapreduce.Job:  map 9% reduce 0%
17/11/28 17:00:14 INFO mapreduce.Job:  map 11% reduce 0%
17/11/28 17:00:20 INFO mapreduce.Job:  map 13% reduce 0%
17/11/28 17:00:26 INFO mapreduce.Job:  map 14% reduce 0%
17/11/28 17:00:32 INFO mapreduce.Job:  map 17% reduce 0%
17/11/28 17:00:38 INFO mapreduce.Job:  map 18% reduce 0%
17/11/28 17:00:44 INFO mapreduce.Job:  map 20% reduce 0%
17/11/28 17:00:50 INFO mapreduce.Job:  map 23% reduce 0%
17/11/28 17:00:57 INFO mapreduce.Job:  map 25% reduce 0%
17/11/28 17:01:04 INFO mapreduce.Job:  map 27% reduce 0%
17/11/28 17:01:10 INFO mapreduce.Job:  map 30% reduce 0%
17/11/28 17:01:16 INFO mapreduce.Job:  map 31% reduce 0%
17/11/28 17:01:22 INFO mapreduce.Job:  map 33% reduce 0%
17/11/28 17:01:28 INFO mapreduce.Job:  map 35% reduce 0%
17/11/28 17:01:34 INFO mapreduce.Job:  map 37% reduce 0%
17/11/28 17:01:41 INFO mapreduce.Job:  map 40% reduce 0%
17/11/28 17:01:46 INFO mapreduce.Job:  map 42% reduce 0%
17/11/28 17:01:53 INFO mapreduce.Job:  map 44% reduce 0%
17/11/28 17:01:59 INFO mapreduce.Job:  map 46% reduce 0%
17/11/28 17:02:05 INFO mapreduce.Job:  map 48% reduce 0%
17/11/28 17:02:11 INFO mapreduce.Job:  map 50% reduce 0%
17/11/28 17:02:17 INFO mapreduce.Job:  map 53% reduce 0%
17/11/28 17:02:23 INFO mapreduce.Job:  map 55% reduce 0%
17/11/28 17:02:29 INFO mapreduce.Job:  map 57% reduce 0%
17/11/28 17:02:35 INFO mapreduce.Job:  map 59% reduce 0%
17/11/28 17:02:41 INFO mapreduce.Job:  map 61% reduce 0%
17/11/28 17:02:47 INFO mapreduce.Job:  map 63% reduce 0%
17/11/28 17:02:54 INFO mapreduce.Job:  map 64% reduce 0%
17/11/28 17:02:55 INFO mapreduce.Job:  map 66% reduce 0%
17/11/28 17:03:00 INFO mapreduce.Job:  map 68% reduce 0%
17/11/28 17:03:08 INFO mapreduce.Job:  map 72% reduce 0%
17/11/28 17:03:14 INFO mapreduce.Job:  map 74% reduce 0%
17/11/28 17:03:21 INFO mapreduce.Job:  map 78% reduce 0%
17/11/28 17:03:26 INFO mapreduce.Job:  map 81% reduce 0%
17/11/28 17:03:32 INFO mapreduce.Job:  map 83% reduce 0%
17/11/28 17:03:38 INFO mapreduce.Job:  map 87% reduce 0%
17/11/28 17:03:46 INFO mapreduce.Job:  map 90% reduce 0%
17/11/28 17:03:52 INFO mapreduce.Job:  map 94% reduce 0%
17/11/28 17:03:57 INFO mapreduce.Job:  map 97% reduce 0%
17/11/28 17:03:58 INFO mapreduce.Job:  map 99% reduce 0%
17/11/28 17:04:00 INFO mapreduce.Job:  map 100% reduce 0%
17/11/28 17:04:03 INFO mapreduce.Job: Job job_1511823443481_0002 completed successfully
17/11/28 17:04:03 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=581340
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=1070139
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=1070139
                Total vcore-milliseconds taken by all map tasks=1070139
                Total megabyte-milliseconds taken by all map tasks=1095822336
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1303
                CPU time spent (ms)=142300
                Physical memory (bytes) snapshot=717156352
                Virtual memory (bytes) snapshot=6329487360
                Total committed heap usage (bytes)=1569718272
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    4m53.095s
user    0m6.386s
sys     0m0.403s


```

### Terasort
```

[jlusancheza@ip-10-0-3-126 centos]$  time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-mapreduce-examples-2.6.0-cdh5.12.1.jar  terasort /user/jlusancheza/teragen-10Gb /user/jlusancheza/terasort-10Gb
17/11/28 17:08:30 INFO terasort.TeraSort: starting
17/11/28 17:08:31 INFO input.FileInputFormat: Total input paths to process : 4
Spent 260ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 266ms
Sampling 10 splits of 300
Making 12 from 100000 sampled records
Computing parititions took 591ms
Spent 859ms computing partitions.
17/11/28 17:08:32 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-3-126.ec2.internal/10.0.3.126:8032
17/11/28 17:08:32 INFO mapreduce.JobSubmitter: number of splits:300
17/11/28 17:08:33 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1511823443481_0003
17/11/28 17:08:33 INFO impl.YarnClientImpl: Submitted application application_1511823443481_0003
17/11/28 17:08:33 INFO mapreduce.Job: The url to track the job: http://ip-10-0-3-126.ec2.internal:8088/proxy/application_1511823443481_0003/
17/11/28 17:08:33 INFO mapreduce.Job: Running job: job_1511823443481_0003
17/11/28 17:08:39 INFO mapreduce.Job: Job job_1511823443481_0003 running in uber mode : false
17/11/28 17:08:39 INFO mapreduce.Job:  map 0% reduce 0%
17/11/28 17:08:50 INFO mapreduce.Job:  map 2% reduce 0%
17/11/28 17:08:51 INFO mapreduce.Job:  map 3% reduce 0%
17/11/28 17:08:52 INFO mapreduce.Job:  map 5% reduce 0%
17/11/28 17:08:53 INFO mapreduce.Job:  map 6% reduce 0%
17/11/28 17:08:59 INFO mapreduce.Job:  map 7% reduce 0%
17/11/28 17:09:00 INFO mapreduce.Job:  map 8% reduce 0%
17/11/28 17:09:02 INFO mapreduce.Job:  map 9% reduce 0%
17/11/28 17:09:03 INFO mapreduce.Job:  map 11% reduce 0%
17/11/28 17:09:05 INFO mapreduce.Job:  map 12% reduce 0%
17/11/28 17:09:08 INFO mapreduce.Job:  map 13% reduce 0%
17/11/28 17:09:09 INFO mapreduce.Job:  map 14% reduce 0%
17/11/28 17:09:12 INFO mapreduce.Job:  map 15% reduce 0%
17/11/28 17:09:14 INFO mapreduce.Job:  map 17% reduce 0%
17/11/28 17:09:17 INFO mapreduce.Job:  map 18% reduce 0%
17/11/28 17:09:18 INFO mapreduce.Job:  map 19% reduce 0%
17/11/28 17:09:19 INFO mapreduce.Job:  map 20% reduce 0%
17/11/28 17:09:22 INFO mapreduce.Job:  map 21% reduce 0%
17/11/28 17:09:24 INFO mapreduce.Job:  map 22% reduce 0%
17/11/28 17:09:25 INFO mapreduce.Job:  map 23% reduce 0%
17/11/28 17:09:26 INFO mapreduce.Job:  map 24% reduce 0%
17/11/28 17:09:27 INFO mapreduce.Job:  map 25% reduce 0%
17/11/28 17:09:29 INFO mapreduce.Job:  map 26% reduce 0%
17/11/28 17:09:32 INFO mapreduce.Job:  map 27% reduce 0%
17/11/28 17:09:33 INFO mapreduce.Job:  map 28% reduce 0%
17/11/28 17:09:35 INFO mapreduce.Job:  map 29% reduce 0%
17/11/28 17:09:36 INFO mapreduce.Job:  map 30% reduce 0%
17/11/28 17:09:37 INFO mapreduce.Job:  map 31% reduce 0%
17/11/28 17:09:41 INFO mapreduce.Job:  map 32% reduce 0%
17/11/28 17:09:43 INFO mapreduce.Job:  map 33% reduce 0%
17/11/28 17:09:44 INFO mapreduce.Job:  map 34% reduce 0%
17/11/28 17:09:45 INFO mapreduce.Job:  map 35% reduce 0%
17/11/28 17:09:46 INFO mapreduce.Job:  map 36% reduce 0%
17/11/28 17:09:51 INFO mapreduce.Job:  map 37% reduce 0%
17/11/28 17:09:52 INFO mapreduce.Job:  map 38% reduce 0%
17/11/28 17:09:53 INFO mapreduce.Job:  map 39% reduce 0%
17/11/28 17:09:54 INFO mapreduce.Job:  map 40% reduce 0%
17/11/28 17:09:55 INFO mapreduce.Job:  map 41% reduce 0%
17/11/28 17:09:58 INFO mapreduce.Job:  map 42% reduce 0%
17/11/28 17:10:01 INFO mapreduce.Job:  map 43% reduce 0%
17/11/28 17:10:02 INFO mapreduce.Job:  map 44% reduce 0%
17/11/28 17:10:03 INFO mapreduce.Job:  map 45% reduce 0%
17/11/28 17:10:05 INFO mapreduce.Job:  map 47% reduce 0%
17/11/28 17:10:06 INFO mapreduce.Job:  map 48% reduce 0%
17/11/28 17:10:09 INFO mapreduce.Job:  map 49% reduce 0%
17/11/28 17:10:11 INFO mapreduce.Job:  map 50% reduce 0%
17/11/28 17:10:14 INFO mapreduce.Job:  map 51% reduce 0%
17/11/28 17:10:15 INFO mapreduce.Job:  map 52% reduce 0%
17/11/28 17:10:16 INFO mapreduce.Job:  map 53% reduce 0%
17/11/28 17:10:17 INFO mapreduce.Job:  map 54% reduce 0%
17/11/28 17:10:19 INFO mapreduce.Job:  map 55% reduce 0%
17/11/28 17:10:21 INFO mapreduce.Job:  map 56% reduce 0%
17/11/28 17:10:24 INFO mapreduce.Job:  map 57% reduce 0%
17/11/28 17:10:25 INFO mapreduce.Job:  map 59% reduce 0%
17/11/28 17:10:27 INFO mapreduce.Job:  map 60% reduce 0%
17/11/28 17:10:30 INFO mapreduce.Job:  map 61% reduce 0%
17/11/28 17:10:31 INFO mapreduce.Job:  map 62% reduce 0%
17/11/28 17:10:33 INFO mapreduce.Job:  map 63% reduce 0%
17/11/28 17:10:35 INFO mapreduce.Job:  map 64% reduce 0%
17/11/28 17:10:36 INFO mapreduce.Job:  map 65% reduce 0%
17/11/28 17:10:37 INFO mapreduce.Job:  map 66% reduce 0%
17/11/28 17:10:40 INFO mapreduce.Job:  map 67% reduce 0%
17/11/28 17:10:42 INFO mapreduce.Job:  map 69% reduce 0%
17/11/28 17:10:45 INFO mapreduce.Job:  map 70% reduce 0%
17/11/28 17:10:46 INFO mapreduce.Job:  map 71% reduce 0%
17/11/28 17:10:47 INFO mapreduce.Job:  map 72% reduce 0%
17/11/28 17:10:49 INFO mapreduce.Job:  map 73% reduce 0%
17/11/28 17:10:51 INFO mapreduce.Job:  map 74% reduce 0%
17/11/28 17:10:54 INFO mapreduce.Job:  map 75% reduce 0%
17/11/28 17:10:55 INFO mapreduce.Job:  map 76% reduce 0%
17/11/28 17:10:57 INFO mapreduce.Job:  map 78% reduce 0%
17/11/28 17:10:59 INFO mapreduce.Job:  map 79% reduce 0%
17/11/28 17:11:00 INFO mapreduce.Job:  map 80% reduce 0%
17/11/28 17:11:05 INFO mapreduce.Job:  map 81% reduce 0%
17/11/28 17:11:06 INFO mapreduce.Job:  map 82% reduce 0%
17/11/28 17:11:07 INFO mapreduce.Job:  map 83% reduce 0%
17/11/28 17:11:08 INFO mapreduce.Job:  map 84% reduce 0%
17/11/28 17:11:09 INFO mapreduce.Job:  map 85% reduce 0%
17/11/28 17:11:11 INFO mapreduce.Job:  map 86% reduce 0%
17/11/28 17:11:18 INFO mapreduce.Job:  map 87% reduce 0%
17/11/28 17:11:19 INFO mapreduce.Job:  map 88% reduce 0%
17/11/28 17:11:22 INFO mapreduce.Job:  map 88% reduce 2%
17/11/28 17:11:24 INFO mapreduce.Job:  map 89% reduce 2%
17/11/28 17:11:25 INFO mapreduce.Job:  map 89% reduce 10%
17/11/28 17:11:26 INFO mapreduce.Job:  map 91% reduce 21%
17/11/28 17:11:32 INFO mapreduce.Job:  map 92% reduce 22%
17/11/28 17:11:33 INFO mapreduce.Job:  map 93% reduce 22%
17/11/28 17:11:36 INFO mapreduce.Job:  map 94% reduce 22%
17/11/28 17:11:37 INFO mapreduce.Job:  map 94% reduce 23%
17/11/28 17:11:39 INFO mapreduce.Job:  map 95% reduce 23%
17/11/28 17:11:40 INFO mapreduce.Job:  map 96% reduce 23%
17/11/28 17:11:43 INFO mapreduce.Job:  map 97% reduce 24%
17/11/28 17:11:46 INFO mapreduce.Job:  map 98% reduce 24%
17/11/28 17:11:47 INFO mapreduce.Job:  map 99% reduce 24%
17/11/28 17:11:49 INFO mapreduce.Job:  map 100% reduce 24%
17/11/28 17:11:50 INFO mapreduce.Job:  map 100% reduce 25%
17/11/28 17:11:52 INFO mapreduce.Job:  map 100% reduce 26%
17/11/28 17:11:55 INFO mapreduce.Job:  map 100% reduce 36%
17/11/28 17:11:56 INFO mapreduce.Job:  map 100% reduce 51%
17/11/28 17:11:58 INFO mapreduce.Job:  map 100% reduce 54%
17/11/28 17:12:01 INFO mapreduce.Job:  map 100% reduce 57%
17/11/28 17:12:02 INFO mapreduce.Job:  map 100% reduce 61%
17/11/28 17:12:03 INFO mapreduce.Job:  map 100% reduce 69%
17/11/28 17:12:07 INFO mapreduce.Job:  map 100% reduce 70%
17/11/28 17:12:08 INFO mapreduce.Job:  map 100% reduce 72%
17/11/28 17:12:09 INFO mapreduce.Job:  map 100% reduce 78%
17/11/28 17:12:10 INFO mapreduce.Job:  map 100% reduce 79%
17/11/28 17:12:13 INFO mapreduce.Job:  map 100% reduce 80%
17/11/28 17:12:14 INFO mapreduce.Job:  map 100% reduce 84%
17/11/28 17:12:15 INFO mapreduce.Job:  map 100% reduce 89%
17/11/28 17:12:19 INFO mapreduce.Job:  map 100% reduce 90%
17/11/28 17:12:20 INFO mapreduce.Job:  map 100% reduce 92%
17/11/28 17:12:21 INFO mapreduce.Job:  map 100% reduce 94%
17/11/28 17:12:26 INFO mapreduce.Job:  map 100% reduce 96%
17/11/28 17:12:27 INFO mapreduce.Job:  map 100% reduce 99%
17/11/28 17:12:34 INFO mapreduce.Job:  map 100% reduce 100%
17/11/28 17:12:45 INFO mapreduce.Job: Job job_1511823443481_0003 completed successfully
17/11/28 17:12:45 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4470888861
                FILE: Number of bytes written=8892085105
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000043800
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=936
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=24
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=12
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=2647343
                Total time spent by all reduces in occupied slots (ms)=826093
                Total time spent by all map tasks (ms)=2647343
                Total time spent by all reduce tasks (ms)=826093
                Total vcore-milliseconds taken by all map tasks=2647343
                Total vcore-milliseconds taken by all reduce tasks=826093
                Total megabyte-milliseconds taken by all map tasks=2710879232
                Total megabyte-milliseconds taken by all reduce tasks=845919232
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4375310728
                Input split bytes=43800
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4375310728
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =3600
                Failed Shuffles=0
                Merged Map outputs=3600
                GC time elapsed (ms)=37150
                CPU time spent (ms)=1553660
                Physical memory (bytes) snapshot=166201024512
                Virtual memory (bytes) snapshot=495203950592
                Total committed heap usage (bytes)=168005468160
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
17/11/28 17:12:45 INFO terasort.TeraSort: done

real    4m16.054s
user    0m8.592s
sys     0m0.500s


```