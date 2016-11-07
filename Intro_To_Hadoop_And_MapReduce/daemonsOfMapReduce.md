#Daemons Of MapReduce

A **Daemon** is a piece of code running all the time on each of the machines in the cluster

A **Data Node** is an individual piece of a file in HDFS stored on a machine in the cluster

The **NameNode** is the node responsible for keeping track of the locations of all the Data Nodes that make up the files stored in HDFS

-

When you run a MapReduce Job you submit the job to a **Job Tracker** that splits the work into Mappers and Reducers that will run on other nodes in the cluster

Running the actual Map and Reduce tasks is handled by a daemon called a **Task Tracker**

The Task Tracker will run on each of the nodes in the cluster telling them to Shuffle, Sort, and Reduce the Intermediate Records