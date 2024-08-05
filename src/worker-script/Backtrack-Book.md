
 
**New Amazon Aurora Backtrack**
 Today I would like to tell you about the new backtrack feature for Amazon Aurora. This is as close as we can come, given present-day technology, to an Undo option for reality.
 
This feature can be enabled at launch time for all newly-launched Aurora database clusters. To enable it, you simply specify how far back in time you might want to rewind, and use the database as usual (this is on the **Configure advanced settings** page):
 
**Download ✓✓✓ [https://kneedacexbrew.blogspot.com/?d=2A0Ofa](https://kneedacexbrew.blogspot.com/?d=2A0Ofa)**


 
Aurora uses a distributed, log-structured storage system (read Design Considerations for High Throughput Cloud-Native Relational Databases to learn a lot more); each change to your database generates a new log record, identified by a Log Sequence Number (LSN). Enabling the backtrack feature provisions a FIFO buffer in the cluster for storage of LSNs. This allows for quick access and recovery times measured in seconds.
 
Then you wait for the rewind to take place, unpause your application and proceed as if nothing had happened. When you initiate a backtrack, Aurora will pause the database, close any open connections, drop uncommitted writes, and wait for the backtrack to complete. Then it will resume normal operation and be able to accept requests. The instance state will be **backtracking** while the rewind is underway:
 
If it turns out that you went back a bit too far, you can backtrack to a later time. Other Aurora features such as cloning, backups, and restores continue to work on an instance that has been configured for backtrack.
 
**Things to Know**
 This option applies to newly created MySQL-compatible Aurora database clusters and to MySQL-compatible clusters that have been restored from a backup. You must opt-in when you create or restore a cluster; you cannot enable it for a running cluster.
 
Backtracking "rewinds" the DB cluster to the time you specify. Backtracking is not a replacement for backing up your DB cluster so that you can restore it to a point in time. However, backtracking provides the following advantages over traditional backup and restore:
 
You can easily undo mistakes. If you mistakenly perform a destructive action, such as a DELETE without a WHERE clause, you can backtrack the DB cluster to a time before the destructive action with minimal interruption of service.

You can backtrack a DB cluster quickly. Restoring a DB cluster to a point in time launches a new DB cluster and restores it from backup data or a DB cluster snapshot, which can take hours. Backtracking a DB cluster doesn't require a new DB cluster and rewinds the DB cluster in minutes.
 
You can explore earlier data changes. You can repeatedly backtrack a DB cluster back and forth in time to help determine when a particular data change occurred. For example, you can backtrack a DB cluster three hours and then backtrack forward in time one hour. In this case, the backtrack time is two hours before the original time.
 
The target backtrack window is the amount of time you want to be able to backtrack your DB cluster. When you enable backtracking, you specify a target backtrack window. For example, you might specify a target backtrack window of 24 hours if you want to be able to backtrack the DB cluster one day.
 
The actual backtrack window is the actual amount of time you can backtrack your DB cluster, which can be smaller than the target backtrack window. The actual backtrack window is based on your workload and the storage available for storing information about database changes, called change records.
 
As you make updates to your Aurora DB cluster with backtracking enabled, you generate change records. Aurora retains change records for the target backtrack window, and you pay an hourly rate for storing them. Both the target backtrack window and the workload on your DB cluster determine the number of change records you store. The workload is the number of changes you make to your DB cluster in a given amount of time. If your workload is heavy, you store more change records in your backtrack window than you do if your workload is light.
 
You can think of your target backtrack window as the goal for the maximum amount of time you want to be able to backtrack your DB cluster. In most cases, you can backtrack the maximum amount of time that you specified. However, in some cases, the DB cluster can't store enough change records to backtrack the maximum amount of time, and your actual backtrack window is smaller than your target. Typically, the actual backtrack window is smaller than the target when you have extremely heavy workload on your DB cluster. When your actual backtrack window is smaller than your target, we send you a notification.
 
When backtracking is enabled for a DB cluster, and you delete a table stored in the DB cluster, Aurora keeps that table in the backtrack change records. It does this so that you can revert back to a time before you deleted the table. If you don't have enough space in your backtrack window to store the table, the table might be removed from the backtrack change records eventually.
 
Aurora always backtracks to a time that is consistent for the DB cluster. Doing so eliminates the possibility of uncommitted transactions when the backtrack is complete. When you specify a time for a backtrack, Aurora automatically chooses the nearest possible consistent time. This approach means that the completed backtrack might not exactly match the time you specify, but you can determine the exact time for a backtrack by using the describe-db-cluster-backtracks AWS CLI command. For more information, see Retrieving existing backtracks.
 
Backtracking is only available for DB clusters that were created with the Backtrack feature enabled. You can't modify a DB cluster to enable the Backtrack feature. You can enable the Backtrack feature when you create a new DB cluster or restore a snapshot of a DB cluster.
 
You can't create cross-Region read replicas from a backtrack-enabled cluster, but you can still enable binary log (binlog) replication on the cluster. If you try to backtrack a DB cluster for which binary logging is enabled, an error typically occurs unless you choose to force the backtrack. Any attempts to force a backtrack will break downstream read replicas and interfere with other operations such as blue/green deployments.
 
You can't backtrack a database clone to a time before that database clone was created. However, you can use the original database to backtrack to a time before the clone was created. For more information about database cloning, see Cloning a volume for an Amazon Aurora DB cluster.
 
Backtracking causes a brief DB instance disruption. You must stop or pause your applications before starting a backtrack operation to ensure that there are no new read or write requests. During the backtrack operation, Aurora pauses the database, closes any open connections, and drops any uncommitted reads and writes. It then waits for the backtrack operation to complete.
 
For the target backtrack window, specify the amount of time that you want to be able to rewind your database using Backtrack. Aurora tries to retain enough change records to support that window of time.
 
You can use the console to configure backtracking when you create a new DB cluster. You can also modify a DB cluster to change the backtrack window for a backtrack-enabled cluster. If you turn off backtracking entirely for a cluster by setting the backtrack window to 0, you can't enable backtrack again for that cluster.
 
When you create a new Aurora MySQL DB cluster, backtracking is configured when you choose **Enable Backtrack** and specify a **Target Backtrack window** value that is greater than zero in the **Backtrack** section.
 
When you create a new DB cluster, Aurora has no data for the DB cluster's workload. So it can't estimate a cost specifically for the new DB cluster. Instead, the console presents a typical user cost for the specified target backtrack window based on a typical workload. The typical cost is meant to provide a general reference for the cost of the Backtrack feature.
 
Currently, you can modify backtracking only for a DB cluster that has the Backtrack feature enabled. The **Backtrack** section doesn't appear for a DB cluster that was created with the Backtrack feature disabled or if the Backtrack feature has been disabled for the DB cluster.
 
When you create a new Aurora MySQL DB cluster using the create-db-cluster AWS CLI command, backtracking is configured when you specify a --backtrack-window value that is greater than zero. The --backtrack-window value specifies the target backtrack window. For more information, see Creating an Amazon Aurora DB cluster.
 
When you create a new Aurora MySQL DB cluster using the CreateDBCluster Amazon RDS API operation, backtracking is configured when you specify a BacktrackWindow value that is greater than zero. The BacktrackWindow value specifies the target backtrack window for the DB cluster specified in the DBClusterIdentifier value. For more information, see Creating an Amazon Aurora DB cluster.
 
You can backtrack a DB cluster to a specified backtrack time stamp. If the backtrack time stamp isn't earlier than the earliest possible backtrack time, and isn't in the future, the DB cluster is backtracked to that time stamp.
 
Otherwise, an error typically occurs. Also, if you try to backtrack a DB cluster for which binary logging is enabled, an error typically occurs unless you've chosen to force the backtrack to occur. Forcing a backtrack to occur can interfere with other operations that use binary logging.
 
Backtracking doesn't generate binlog entries for the changes that it makes. If you have binary logging enabled for the DB cluster, backtracking might not be compatible with your binlog implementation.
 
For data