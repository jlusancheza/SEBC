# Yarn Test 

```
#!/bin/sh
#Confirm the path values given below correspond to your installation

MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
HADOOP=/opt/cloudera/parcels/CDH/bin

# Mark start of the loop
echo Testing loop started on `date`

# Mapper containers
for i in 3 5
do
   # Reducer containers
   for j in 3 5
   do
      # Container memory
      for k in 1024 2048
      do
         # Set mapper JVM heap
         MAP_MB=`echo "($k*0.8)/1" | bc`

         # Set reducer JVM heap
         RED_MB=`echo "($k*0.8)/1" | bc`
        echo "Teragen: mapreduce.job.maps=$i, mapreduce.job.memory=$k mapreduce.map.java.opts.max.heap=$MAP_MB"
        time ${HADOOP}/hadoop jar ${MR}/hadoop-examples.jar teragen \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     51200000 results/tg-10GB-${i}-${j}-${k} 1>tera_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err
        echo "  "
        echo "Terasort: mapreduce.job.maps=$i, mapreduce.job.reduces=$j,mapreduce.map.memory.mb=$k"
        echo "mapreduce.map.java.opts.max.heap=$MAP_MB,mapreduce.reduce.memory.mb=$k,mapreduce.reduce.java.opts.max.heap=$RED_MB "
        time ${HADOOP}/hadoop jar $MR/hadoop-examples.jar terasort \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.job.reduces=$j \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     -Dmapreduce.reduce.memory.mb=$k \
                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
                     results/tg-10GB-${i}-${j}-${k}  \
               results/ts-10GB-${i}-${j}-${k} 1>>tera_${i}_${j}_${k}.out 2>>tera_${i}_${j}_${k}.err
        echo "-------------------------------------------------------------------------------------------------"
        $HADOOP/hdfs dfs -rm -r -skipTrash results/tg-10GB-${i}-${j}-${k}
        $HADOOP/hdfs dfs -rm -r -skipTrash results/ts-10GB-${i}-${j}-${k}
      done
   done
done

echo Testing loop ended on `date`

```