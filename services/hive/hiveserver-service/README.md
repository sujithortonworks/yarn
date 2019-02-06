Ran similar commands as follows:
cp -r /usr/hdp/3.1.0.0-78/hive /tmp
made some changes for HIVE_HOME etc, create log etc folders. used existing keytabs etc
tar -zcvf hive.tgz /tmp/hive
hdfs dfs -put hive.tgz /user/hive/
yarn app -launch hiveserver-service hiveserver.json
yarn app -status hiveserver-service
yarn app -destroy hiveserver-service
