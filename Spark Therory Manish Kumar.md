>> ### Spark
*   Spark : Unified computing engine.

*   Spark's worker nodes don't have memory of their own.

>> ### Hadoop vs Spark

*   Hadoop is NOT database.
*   Spark is NOT 100X faster but **upto**.
*   *Misconception* -> Hadoop don't process in RAM.
*   Hadoop was built for batch data processing.
*   Hive -> SQL queries for Hadoop. **STILL DIFFICULT** to code.
*   Spark -> Python, java scala API.
*   *Security* : In Hadoop kerboroes and YARN for authorization and authetication. vs In Spark when it uses HDFS and YARN.
*   Fault Tolerance : HDFS have replication factor usally 3. 

    |     | Hadoop   | Spark    |
    |--------------|--------------|--------------|
    | Fault Tolerance | HDFS have replication factor usally 3. So data will be distributed on 3 nodes  | Spark used **DAG**. For each process it will save an immutable RDD |
    | Security  | YARN and Kerboses | No but used Hadoop's|
    | Why? | Difficult, slow | Easy, fast |


>> ### Why Spark is faster?
It reads from RAM and write in RAM where as Hadoop Read and write on Disk ROM.

![Hadoop vs Spark](<Hadoop vs Spark.png>)




>> ### Spark Architecture

<br>
<br>

![alt text](Spark%20Architecture.png)

<br>

![alt text](/Resource-cluster%20Manager.png)





>> ### How it works ?

*  Cluster-10 -> 1 : Master Node + 9 : Worker Node

*  Developer will submit code to RM.
with details like
    1.  Driver : 20GB
    2.  excecutor -25 GB and 5 core.
    3.  Number of executor - 5


* *We should not use UDF (Code in pure python), because it will require Python worker to execute and can slow down process.*


*   The **RM** is responsible for managing the cluster resources. (CPU, memory). e.g YARN, Kubernetes.

*   The **Driver** is the main process that runs your Spark application. It is responsible for coordinating the job’s execution and managing the job’s overall lifecycle.

* Each **Executor** is responsible for reading data, performing computations, and storing the results for the tasks assigned to it.

* If the data is stored externally (e.g., in HDFS, S3, or a database), Executor 1 will directly read the data from the source as per the instructions it received from the Driver. 










