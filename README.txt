1-
Copy the input.txt (dataset) to HDFS.
use : /PATH-TO-HADOOP/bin/hadoop dfs -put /PATH-TO-INPUT-FILE/input.txt /
---------------------------------------------------------------------------------------------------------------------
2-
Compile Friend.java(inside DATA folder).
use : /PATH-TO-HADOOP/bin/hadoop com.sun.tools.javac.Main /PATH-TO-JAVA-FILE/Friend.java
---------------------------------------------------------------------------------------------------------------------
3-
Make a JAR file from the resulting class files.
use : jar cf NAME-OF-JAR-FILE.jar Friend*.class
Run the above command in the directory where the class files are stored.
---------------------------------------------------------------------------------------------------------------------
4-
Run MapReduce on the file.
use : /PATH-TO-HADOOP/bin/hadoop jar /PATH-TO-JAR-FILE/Friend.jar Friend /input.txt /OutputFolder
---------------------------------------------------------------------------------------------------------------------
5-
Output is located in /OutputFolder/part-* file in HDFS. To view,
use : /PATH-TO-HADOOP/bin/hadoop dfs -cat /OutputFolder/part-00000
considering output is in file named 'part-0000'.
---------------------------------------------------------------------------------------------------------------------
