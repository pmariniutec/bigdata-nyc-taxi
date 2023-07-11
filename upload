#!/bin/bash

export JAVA_HOME=/usr/lib/jvm/default
export HADOOP_USER_NAME=hadoopuser

./bin/hdfs dfs -mkdir "hdfs://20.121.35.246:9000/nyc_trips"

for filename in ../nyc_trips/*.parquet; do
  sleep 4
  echo "Uploading ${filename}"
  ./bin/hdfs dfs -put $filename "hdfs://20.121.35.246:9000/nyc_trips/"
done
