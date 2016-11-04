#Hadoop Distributed File System

Data files are stored in the HDFS which, from a high level, looks like a regular file system but behind the scenes behaves differently

Example:

If we were to store a file called "myData.txt" that was 150mb in HDFS, it would be split into chunks that we call blocks that are fairly large (64mb by default)

Each block is labeled "blk_X" where "X" is the index assigned to a particular block upon loading the source file into HDFS

```
mydata.txt (150mb)

      ________
blk_1 | 64mb |
      |______|
blk_2 | 64mb |
      |______|
blk_3 | 22mb |
      --------
```

As the file is uploaded to HDFS each block will be represented by a single node in the cluster

There is a **daemon**, or piece of software, running on each of the machines in the cluster called the datanode

-

###Namenode

The **Namenode** keeps track of which nodes in the cluster make up a whole file in the HDFS. The information stored in the Namenode is known as the **metadata**

When a file is uploaded into HDFS, after the file is split into different blocks, two copies of each block are created and stored in other nodes so that if you lose one node then the Namenode can just use the copies instead and create more copies to replace the lost node

