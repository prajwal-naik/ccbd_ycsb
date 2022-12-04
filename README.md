# ccbd_ycsb

To drop the db:


Open mongo shell by typing the command,

`mongo`


In the mongo shell, run the following commands:

`show databases`

`use yscb`			

`db dropDatabase()`



Note: In the above commands, yscb is the name of the database.

Exit the mongo shell.





To load the data:

`./bin/ycsb load mongodb -s -P workloads/workloada -t -p recordcount=100000 -threads 16 -p mongodb.url="mongodb://localhost:27017/ycsb" -p mongodb.auth="true"`



To execute the workload:

For workloads A,B and C -

./bin/ycsb run mongodb -s -t -P workloads/<workload> -p operationcount=<recordcount> -threads 16 -p mongodb.url="mongodb://localhost:27017/yscb" -p mongodb.auth="true"


For workloads D, E and F -

./bin/ycsb run mongodb -s -t -P workloads/<workload> -p recordcount=<recordcount> -p operationcount=<recordcount> -threads 16 -p mongodb.url="mongodb://localhost:27017/yscb" -p mongodb.auth="true"





Note: The workload was varied from workloada to workloadf and the value of recordcount was varied from 100000 to 500000.


The values of throughput and latency were recorded and the required graphs were plotted.
