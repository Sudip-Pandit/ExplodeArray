# ExplodeArray
Explode Array Column in Complex data processing


# Output is:
2022-03-26 07:54:41 INFO  BlockManagerMaster:54 - Registering BlockManager BlockManagerId(driver, DESKTOP-7A8PRJV, 54226, None)
2022-03-26 07:54:41 INFO  BlockManagerMasterEndpoint:54 - Registering block manager DESKTOP-7A8PRJV:54226 with 1970.4 MB RAM, BlockManagerId(driver, DESKTOP-7A8PRJV, 54226, None)
2022-03-26 07:54:41 INFO  BlockManagerMaster:54 - Registered BlockManager BlockManagerId(driver, DESKTOP-7A8PRJV, 54226, None)
2022-03-26 07:54:41 INFO  BlockManager:54 - Initialized BlockManager: BlockManagerId(driver, DESKTOP-7A8PRJV, 54226, None)
2022-03-26 07:54:42 INFO  ContextHandler:781 - Started o.s.j.s.ServletContextHandler@ba1f559{/metrics/json,null,AVAILABLE,@Spark}
+--------------------+--------------------+--------+--------+
|            Students|             address| orgname| trainer|
+--------------------+--------------------+--------+--------+
|[[[56, srini]], [...|[Hyderabad, Chennai]|zeyobron|Sudipeee|
+--------------------+--------------------+--------+--------+

root
 |-- Students: array (nullable = true)
 |    |-- element: struct (containsNull = true)
 |    |    |-- user: struct (nullable = true)
 |    |    |    |-- age: long (nullable = true)
 |    |    |    |-- name: string (nullable = true)
 |-- address: struct (nullable = true)
 |    |-- permanentAddress: string (nullable = true)
 |    |-- temporaryAddress: string (nullable = true)
 |-- orgname: string (nullable = true)
 |-- trainer: string (nullable = true)

+-------------+--------------------+--------+--------+
|     Students|             address| orgname| trainer|
+-------------+--------------------+--------+--------+
|[[56, srini]]|[Hyderabad, Chennai]|zeyobron|Sudipeee|
| [[45, anil]]|[Hyderabad, Chennai]|zeyobron|Sudipeee|
+-------------+--------------------+--------+--------+

root
 |-- Students: struct (nullable = true)
 |    |-- user: struct (nullable = true)
 |    |    |-- age: long (nullable = true)
 |    |    |-- name: string (nullable = true)
 |-- address: struct (nullable = true)
 |    |-- permanentAddress: string (nullable = true)
 |    |-- temporaryAddress: string (nullable = true)
 |-- orgname: string (nullable = true)
 |-- trainer: string (nullable = true)

+---+-----+----------------+----------------+--------+--------+
|age| name|permanentAddress|temporaryAddress| orgname| trainer|
+---+-----+----------------+----------------+--------+--------+
| 56|srini|       Hyderabad|         Chennai|zeyobron|Sudipeee|
| 45| anil|       Hyderabad|         Chennai|zeyobron|Sudipeee|
+---+-----+----------------+----------------+--------+--------+

root
 |-- age: long (nullable = true)
 |-- name: string (nullable = true)
 |-- permanentAddress: string (nullable = true)
 |-- temporaryAddress: string (nullable = true)
 |-- orgname: string (nullable = true)
 |-- trainer: string (nullable = true)
