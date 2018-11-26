Spring Transaction Management

Spring uses AOP for transaction management. It happens under the hood.AOP allows you define Cross Cutting Concerns. Because we want to apply Transaction management on many services at the same time.
Cross Cutting Concern means for example Logging, Security, Transaction is an Aspect on appears on many places. That’s why we say simply Cross Cutting Concern for them.
Spring creates Proxy class which has begin and commit/rollback. We use Spring TransactionManager which manages Database begin-commit. It takes Datasource as a parameter.

We don’t need to define transaction management on DAO normally. Thats because it is a simple database operation. On Service layer business contains multiple DAO calls. For this reason we define transaction on Service layer.

Best approach is Annotation base approach. 

How to apply;
create bean for org.springframework.datasource.SpringTransactionManager
add tx dtd on xml.
define tx:annotation-driven and set transaction-manager if the bean name is different that simple transactionManager by default.
Spring will scan all bean defined in xml and look for @Transactional
then add @Transaction on the top of the bean.
Spring will create TransactionProxy class.
Now all method of service has begin and commit on a service which has @Transactional
If the service has 100 methods, all methods will have transaction behaviour
Alternatively we can add @Transactional on top of method, only the method will have it
We have add @Transactional only on the Bean which call DB beans.
Adding Spring TransactionManager set JDBC default auto-commit to false.

We use annotation driven transaction rather than xml based because transaction can’t change often like app performance timing. 

Transaction manager only works with transaction data store for example database. 