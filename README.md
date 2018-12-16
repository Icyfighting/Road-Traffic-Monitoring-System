# Road-Traffic-Monitoring-System
This project is training project that I completed in programing school.
The project is road traffic monitoring system. It provides analysis of intersection traffic, car path track,
topN highest traffic statistics for each region, road real-time congestion statistics,real-time car blacklist.
****
    
|Author|Bing Yan|
|---|---
|E-mail|187233718@qq.com


****
## Table of Contents
* [Functions Introduction](#Functions-Introduction)
    * [Intersection Traffic Analysis](#Intersection-Traffic-Analysis)
    * [Car Path Track](#Car-Path-Track)
    * [TopN Highest Traffic](#TopN-Highest-Traffic)
    * [Real-time Congestion](#Real-time-Congestion)
    * [Real-time Car Blacklist](#Real-time-Car-Blacklist)
* [How to run](#How-to-run)
    * [Environment Dependence](#Environment-Dependence)
    * [Deployment Configuration](#Deployment-Configuration)
* [Note](#Note)
### Functions-Introduction
#### Intersection-Traffic-Analysis
```

```
#### Car-Path-Track
```

```
#### TopN-Highest-Traffic
```

```
#### Real-time-Congestion
```

```
#### Real-time-Car-Blacklist
```

```

### How-to-run
#### Environment-Dependence 
```

```
#### Deployment-Configuration
##### Data Simulation
1. For Spark Local mode
```
Set spark.local=true in configuration file src\my.properties
Run main method in src\com\producedate2hive\Data2File.java to generate monitor_camera_info and monitor_flow_action as data
```
2. For Spark Standdalone mode
```
Set spark.local=false in configuration file src\my.properties
Export jar package with main method in src\com\producedate2hive\Data2Hive.java.
Upload exported jar package to Spark cluster.
Run jar package with command spark-submit and generate data in hive.
```
##### Create tables in MySQL database
In MySQL, run src\sql\traffic.sql to geterate tables which to store analysis results.


##### Run task you want
Take task 'intersection flow monitoring' for example:
(Task information can be checked in inserted data of traffic.sql)
1. For Spark Local mode
```
Set spark.local=true in configuration file src\my.properties
Run main method in src\com\bjsxt\spark\skynet\MonitorFlowAnalyze.java to generate analysis results.
Analysis results can be checked in database tables.
```
2. For Spark Standdalone mode
```
Set spark.local=false in configuration file src\my.properties
Export jar package with main class MonitorFlowAnalyze in src\com\bjsxt\spark\skynet\MonitorFlowAnalyze.java
Upload exported jar package to Spark cluster.
Run jar package with command spark-submit and with parameter 1 as task id of task 'intersection flow monitoring'.
Check database table 'task' to confirm task_param with same date with simulated data.
Analysis results can be checked in database tables.
```
### Note
```
The whole project is big, as student we focus on the Spark operator, SparkSQL, Spark Streaming practice.
Teacher provides the framework of project, including util & jdbc & dao & domain in src\com\bjsxt\spark.
As student, we practice partial function in areaRoadFlow & rtmroad & skynet.
```
