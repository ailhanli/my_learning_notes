how transactions are effected by other transactions that are running at the same time.

SERIALIZABLE:  
In this mode, all transaction waits each other. They are querying. Transaction run as serial. One at a time until commit or rollback. Table will locked until commit or rollback. For example if one transaction query table other transaction at the same time cannot update or insert table.
Risk is table lock! that’s why deadlock

REPEATABLE_READ: 
In this mode, only the new records insert from other transaction can be seen which is known as Phantom_Read. It confuses about the primary key id time by time. For example during transaction 2, transaction 1 can insert record id will be next, after transaction if it is it will be second next. 
Risk is phantom read!!
Simply in this mode transaction 1 query results preserved and new insert can be seen. 
System simply cached ids which queried and don’t allow changes about this records.
Table lock is not required.
It perform better than SERIALIZABLE but has phantom risk!

READ_COMMITED:
In this mode all changes from other transaction which run at the same time can seen by other transaction. Imagine several transaction at the same time. On this time record changes will be overlapping.
The risk is Non-Repeatable Read. It mean if one record content is changed by other you cannot see old value. It is rarely used!

READ_UNCOMMITED: 
This is the most dangerous one but more performant. There is no isolation level. 
That why transaction 1 can see other changes without their commit/rollback, in case it rollbacked transaction 1 still can process changes for example it can save it.
Main risk is Dirty Reads

Mysql by default is Repeatable_Read (innoDB engine)
All supported.
Oracle is by default Read_Commited. And Serializable is supported also.
