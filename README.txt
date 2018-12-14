The whole project is big, as student we focus on the Spark operator, SparkSQL, Spark Streaming practice.
Teacher provides the framework of project, including util & jdbc & dao & domain in src\com\bjsxt\spark.
As student, we practice partial function in areaRoadFlow & rtmroad & skynet.

How to run:
1.Data Simulation:
	a.For Spark Local mode: 
		Set spark.local=true in configuration file src\my.properties
		Run main method in src\com\producedate2hive\Data2File.java to generate monitor_camera_info and monitor_flow_action as data
	b.For Spark Standdalone mode:
		Set spark.local=false in configuration file src\my.properties
		Export jar package with main method in src\com\producedate2hive\Data2Hive.java.
		Upload exported jar package to Spark cluster.
		Run jar package with command spark-submit and generate data in hive.

2.Create tables in MySQL database:
	In MySQL, run src\sql\traffic.sql to geterate tables which to store analysis results.

3.Run task you want:
Take task 'intersection flow monitoring' for example:
(Task information can be checked in inserted data of traffic.sql)
	a.For Spark Local mode:
		Set spark.local=true in configuration file src\my.properties
		Run main method in src\com\bjsxt\spark\skynet\MonitorFlowAnalyze.java to generate analysis results.
		Analysis results can be checked in database tables.	
	b.For Spark Standdalone mode:
		Set spark.local=false in configuration file src\my.properties
		Export jar package with main class MonitorFlowAnalyze in src\com\bjsxt\spark\skynet\MonitorFlowAnalyze.java
		Upload exported jar package to Spark cluster.
		Run jar package with command spark-submit and with parameter 1 as task id of task 'intersection flow monitoring'.
		Check database table 'task' to confirm task_param with same date with simulated data.
		Analysis results can be checked in database tables.

