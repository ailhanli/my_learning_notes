A Transaction is a group of operations we want to run as a single unit of work.
We wii never want to situation where some of the operations are applied.
In case of error in some steps of transaction all operation will be reverted. If we decided to not applied changes before commit we can simply use rollback.

JDBC is by default auto-commit. For non-trivial system you don’t want to do this.
It means simply you get an implicit transaction on every single operation.

At least two reasons it is bad;
Reason 1 is impacts performance of your code. Thats because every time commit happens, the database do some hard work to physically commit your data to hdd.
Reason 2 is is loosing ability to rollback transaction. Reason 2 is main reason!!

We have to be sure that Auto-Commit is OFF.

Assume we have two services first one is book service, second one is account service. We we dont provide a service for case buy a book and then raise an invoice, overtime all client should know these steps and in case of changes all have to change their logic. It is very bad. It make clients less cohesive!!!

Application transaction should be on Service layer. Not the on DAO layer. Thats because it is single db operation. Normally we use JTA for this purpose. But it makes code less cohesive now code will have also transaction codes.And we loose side of business process. We want keep method impl. clean. 