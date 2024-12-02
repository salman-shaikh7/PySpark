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

![alt text](Spark%20Architecture.png)



reference 







