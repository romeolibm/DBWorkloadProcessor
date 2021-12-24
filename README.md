# DBWorkloadProcessor
As of 2021-12-24 this logic does not use log4j (Java native logging only) so it is not exposed to CVE-2021-44228.

A set of tools used to cature, analyze workloads, create and execute workload tests for DB2 databases or RDBMS systems in general
To install simply download, check the sha512sum for integrity (optional) then execute
```shell
java -jar rlt_db2wlpt_<build-timestamp>.jar
```

Each build jar contains its own installer as well as the full source code bundled inside of it.

This is done on propose as "open source" should always allow you to trace a binary back to the
source code it was built from. In this case the source is right there are your fingertips
bundled along with the binary implementation.
Because of this strategy the classic git repository is a not used as expected and I'll get back to this
problem later as time permits.

The builds have a life cycle, are first provided as "beta" in the betaBuild folder, those builds
are not verified an a UAT type of environment or by use in a production env for at least one month.
Once a build is declared stable it will be promoted to stable status by moving the file into the 
stableBuild folder (a git rename operation).
If the build is not validated it will simply be removed from the betaBuild folder.
When a stable build is rescinded it will be moved to buildHistory folder (git mv operation).

The solution design is depictred in the diagram bellow:
![Design](workload_processing_system_design.png)

Command: db2_evmon_wlp implementation architecture

![db2_evmon_wlp implementation architecture](db2_evmon_etl_architecture.png)


Command: db2_evmon_wlp implementation multi-threaded architecture

![db2_evmon_wlp implementation MT architecture](db2_evmon_etl_architecture_MT_insert.png)
