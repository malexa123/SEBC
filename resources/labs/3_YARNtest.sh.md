[malexa123@ip-172-31-24-137 tmp]$ cat YARNtest.sh
#!/bin/sh
# Confirm the path values given below correspond to your installation

MR=/opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce
HADOOP=/opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/bin

# Mark start of the loop
echo Testing loop started on `date`

# Mapper containers
for i in 2 4 6
do
   # Reducer containers
   for j in 2 4 6
   do
      # Container memory
      for k in 512 1024
      do
         # Set mapper JVM heap
         MAP_MB=`echo "($k*0.8)/1" | bc`

         # Set reducer JVM heap
         RED_MB=`echo "($k*0.8)/1" | bc`

        # Echo all Variables
        echo "Mapper Container:$i       Reducer Container:$j    Container Memory:$k      Mapper JVM:$MAP_MB      Reducer JVM:$RED_MB"
        echo "time: teragen"
        time ${HADOOP}/hadoop jar ${MR}/hadoop-mapreduce-examples.jar teragen \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     51200000 /user/malexa123/results/tg-10GB-${i}-${j}-${k} >terag_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err
        echo "time: terasort"
       time ${HADOOP}/hadoop jar $MR/hadoop-mapreduce-examples.jar terasort \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.job.reduces=$j \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     -Dmapreduce.reduce.memory.mb=$k \
                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
                     /user/malexa123/results/tg-10GB-${i}-${j}-${k}  \
                     /user/malexa123/resultsX/ts-10GB-${i}-${j}-${k} >teras_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err


        $HADOOP/hadoop fs -rm -r -skipTrash /user/malexa123/results/tg-10GB-${i}-${j}-${k}
        $HADOOP/hadoop fs -rm -r -skipTrash /user/malexa123/resultsX/ts-10GB-${i}-${j}-${k}
      done
   done
done

echo Testing loop ended on `date`
[malexa123@ip-172-31-24-137 tmp]$
