#Basic Hadoop Commands

Hadoop commands closely resemble standard Unix commands

-

> hadoop fs -ls

This will display all the files in the current directory

-

> hadoop fs -put fileName.txt

This will add a file to your directory, this file can be of any extension

-

> hadoop fs -mv fileName.txt

This will move a file to a new directory and will allow you to rename the file

-

> hadoop fs -rm fileName.txt

This will delete the file

-

> hadoop fs -mkdir dirName
> hadoop fs -put fileName.txt dirName
> hadoop fs -ls

This will create a new directory nameed 'dirName', put the "fileName.txt" into that folder, and then display the contents of the directory which will show the "fileName.txt" file and its details