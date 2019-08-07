# DBWorkloadProcessor
A set of tools used to cature, analyze workloads, create and execute workload tests for DB2 databases or RDBMS systems in general
To install simply download, check the sha512sum for integrity (optional) then execute
```shell
java -jar rlt_db2wlpt_<build-timestamp>.jar

sha256sum is 29d26ff2814a4b7d4d40642bd51ac28628c1808d7c7c9409d92335ae1a33fc72
 for rlt_db2wlpt_minimal_2019_08_07_16_05_07_572.jar
```
The solution design is depictred in the diagram bellow:
![Design](workload_processing_system_design.png)

Command: db2_evmon_wlp implementation architecture

![db2_evmon_wlp implementation architecture](db2_evmon_etl_architecture.png)


Command: db2_evmon_wlp implementation multi-threaded architecture

![db2_evmon_wlp implementation MT architecture](db2_evmon_etl_architecture_MT_insert.png)
