# DBWorkloadProcessor
A set of tools used to cature, analyze workloads, create and execute workload tests for DB2 databases or RDBMS systems in general
To install simply download, check the sha512sum for integrity (optional) then execute
```shell
java -jar rlt_db2wlpt_<build-timestamp>.jar

sha256sum is b653972722c0a0cf0db1b3b006dec48fd8e652056d9ab531ec66b3c74188576 for  rlt_db2wlpt_minimal_2019_08_05_14_15_02_630.jar
```
The solution design is depictred in the diagram bellow:
![Design](workload_processing_system_design.png)

Command: db2_evmon_wlp implementation architecture

![db2_evmon_wlp implementation architecture](db2_evmon_etl_architecture.png)


Command: db2_evmon_wlp implementation multi-threaded architecture

![db2_evmon_wlp implementation MT architecture](db2_evmon_etl_architecture_MT_insert.png)
