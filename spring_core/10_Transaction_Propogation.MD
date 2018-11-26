Transaction Propogation
There two types of transaction. These are logical and pychical. Methods from distinc Spring bean maybe execute in same transaction scope or actually being spanned across multiple nested transactions. This may lead how inner transaction outcome results affects the outer transaction


REQUIRED: 
Required means this method requires transaction. If it is called bu the any other method whic has also transactional behavior it will join its transaction. Both share same pychical transaction from transactional store. If if calls directly by the client it will create new pychical transaction.

SUPPORTED: 
Not all methods required transaction. Maybe it make changes in memory or do some business logic.Never talk with transactional store.Supported simply means this method support transaction if it called by transactional method. Otherwise it wont be in transactional state. In case calling supported directly we loose transaction and it will be in auto-commit mode. The main purpose is disabling transaction for the methods who hasnt communicstion with transactional store

NOT_SUPPORT: 
if the method has a problem working as a part of parent transaction we need this level. For example create drop table cant be supported by some dbs in this case we need to use this level to get around work. In this level, method wont support new transaction. How can it be? Spring creates new thread and suspend current transaction. After method call it resume transaction

REQUIRED_NEW: 
it creates brand new transaction. Parent and new transaction completely isolated. Thats why we cant rollback new one in case of rollbacking parent. We can use this for the logging and auditing to table for example for banking app.It is danger for the normal situation.

NEVER: 
if we put this propogation rule on child transaction, it will throws an exception if a transaction is already open. Simply means you cannot use it within transaction.

MANDOTORY:
this propogation rule simply means you can use this method without transaction. It is good for layered app. Commonly it is crucial we put business logic on service layer for data integrety. Without Mandotory rule we will this. 


NESTED:
Others comes from EJB. Thats because Spring use it in a coherent way. This is Spring spesific and cannot be use in hibernate and disturbided transaction.
Simply means when parent calls child transaction which is nested transaction parent will be save point before child. In case child failed parent will restore the save point and continue. If parent rollback child also will be rollback. There will be only one pychical transaction bw child and parent. Use case is if we calling legacy code in our transactional method in case it crashes we keep going on our transaction.


