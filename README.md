# DBWorkloadProcessor
A set of tools used to cature, analyze workloads, create and execute workload tests for DB2 databases or RDBMS systems in general
To install simply download, check the sha512sum for integrity (optional) then execute
```shell
java -jar rlt_db2wlpt_<build-timestamp>.jar
```
sha256sum for rlt_db2wlpt_minimal_2019_05_22_03_22_12_152.jar is: e4998277c108929068481e467f8eb30d3307eb213c04d5b1e4a458b760985967

sha256sum for rlt_db2wlpt_minimal_2019_05_24_17_16_44_263.jar is: 16567130a605ddce63b243c527d9a5738fa089a1810d0622188077d5b448e41f

The solution design is depictred in the diagram bellow:
![Design](workload_processing_system_design.png)

Command: db2_evmon_wlp implementation architecture

![db2_evmon_wlp implementation architecture](db2_evmon_etl_architecture.png)


Command: db2_evmon_wlp implementation multi-threaded architecture

![db2_evmon_wlp implementation MT architecture](db2_evmon_etl_architecture_MT_insert.png)
