#NameNode

The NameNode holds metadata that keeps track of where all the blocks of your datafiles are stored in the cluster

If the NameNode is lost, all the information on the cluster becomes inaccesible

-

To solve this problem you can store the NameNodes metadata in the NameNode AND in a Network File System (NFS) - a method of mounting a remote disk

Now even if the NameNode is lost we will still have the metadata safely stored

-

Even better than NFS, lots of modern companies now have two NameNodes; and active one, and a standby one

If ever the active NameNode fails, the standby one will take over