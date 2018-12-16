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
    * [Test Information](#Test-Information)
* [Note](#Note)
### Functions-Introduction
#### Intersection-Traffic-Analysis
```

```
#### Car-Path-Track
```
Client Management module provides add, delete, update, conditional query operations of clients of this car rental company.
Client information includes ID, name, gender, career, address and so on.
This system is background management system, client information should be operated by user of system.
```
#### TopN-Highest-Traffic
```
Car Management module provides add, delete, update, conditional query operation of car resources in the company.
Car information includes car number, car type, color, rent price, deposit, renting status, description and so on.
```
#### Real-time-Congestion
```
Business Managemnt module includes operation of car renting, car returning, car renting table management and car checking table management.
Each module in business management provide add, conditional query operation according to needs of different business logic.
Car renting module provides operation including conditional car search, renting selected car and selected time.
Car returning module provides operation including returning car with real renting time, renting table creation.
Car renting talbe module provides operation including conditional query of renting record, checking table creation.
Car checking table module provides operation including conditional query of checking table. 
```
#### Real-time-Car-Blacklist
```
System management module includs Role creation, Log searching.
Role creation module provide operation to create a new role by selecting operation permission defined in system.
Log searching module provide operation including login records and operation records defined in interceptor which operation can change data in database.
```

### How-to-run
#### Environment-Dependence 
```
JDK 1.8
Tomcat
MySQL 5.0
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
#### Test-Information
```
user:admin
passwd:a1231
```
### N
```
The whole project is big, as student we focus on the Spark operator, SparkSQL, Spark Streaming practice.
Teacher provides the framework of project, including util & jdbc & dao & domain in src\com\bjsxt\spark.
As student, we practice partial function in areaRoadFlow & rtmroad & skynet.
```
