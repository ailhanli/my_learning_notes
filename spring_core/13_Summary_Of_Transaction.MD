Summary of Transactions

What is transaction?
- Group of operation run as single unit of work. All operation either success or fail. Cant be one of them success other fails.

How is jdbc auto-commit by default?
- By default auto-commit enabled. Auto-commit is evil

Cost of auto-commit
- First cost is persisting data on the disk and it reduce app performance 
The main reason loosing ability of rollback

Where should be transaction in app
in should be service layer. 
- On service layer we call many DAOs. In DAO all methods are single unit of work usually.

How can we applied transaction on code
- JTA can helo us to apply it. But make class less cohesive. Thats because you lose my business logic. SRP violation.

How does it implement in Spring
- Spring uses AOP to apply transaction management. Because it is cross cutting concern. It is concern which cuts many beans. 
Spring AOP simply manages database begin-commit on app layer.
if we mark a class as @Transactional, all methods in this class first will be begin, last line will be commit.

How can we apply transaction in Spring using annotations?
- Firstly we have to define org.springframework.datasource.DataSourceTransactionManager as bean and set DataSource as parameter.
And then add "tx" dtd to xml and simple add <tx:annotation-drive/> and add @Transactional on all service layer which requires
transaction management.
