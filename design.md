
### write request

1. commit it to the log (for data durability)
2. write it to the memtable 
3. regularly make the memtable persistent (that is write it into the SStable in the disk)
    
    3.1 if the memtable is persistent, delete the corresponding commit log (how to delete)
    
### read request

1. read from the memtable using SSTable idx
2. read from the most recent new SSTable
3. read from the least new SSTable 

### creating index for SSTable
1. when to create index for SSTable ?


### crash recovery


### reference 
#### open source project using SSTable 
1. rocksdb 
2. leveldb 
3. Cassandra