#Running A Job

MapReduce code is often written in Java

We will use **Hadoop Streaming** to write our MapReduce code in Python since it is easier to interpret. Hadoop Streaming can be use to write MapReduce code in many different languages.

***

###Syntax for running a hadoop job

hs {mapper script} {reducer script} {input_file} {output directory}

***

###Example of Running a Job

hadoop jar /path/to/jar/file/jarfile.jar -mapper mapper.py -reducer reducer.py -file mapper.py -file reducer.py -input myinput -output joboutput

The above command can be described as: first we say that we are running a hadoop job, then we say that the job is a 'jar' job and direct it to the job jarfile, then we give it a mapper and a reducer, and finally we specify out input and output at the end

-

If we look in the 'joboutput' directory that is created after this job completes, we will find three files

The '_SUCCESS' file indicates that our job ran successfully, the '_logs' directory that contains some logs about the job, and lastly a file called 'part-00000' that is the output from the reducer

-

To look at the output file 'part-00000' we can use:

>hadoop fs -cat joboutput/part-00000 | less

This will view the file with 'less' details so it is easy to read

-

If you want to retreive data from HDFS and put it onto your local disk:

>hadoop fs -get joboutput/part-00000 mylocalfile.txt

The above command will take put the output of the job into a text file on  your local disk

-

#####When running a hadoop job - the output directory must not already exist