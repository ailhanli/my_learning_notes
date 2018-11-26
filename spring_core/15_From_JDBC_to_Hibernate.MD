From JDBC to Hibernate to Spring

Default JDBC API is low level. You need to load driver, open/close connection, create statement, handle exception..etc if you need transaction you also need to use JTA.

Spring has elegant solution to eliminate this this code repetition which is known as boiler plate code. Spring uses Template design pattern. You only need to create your sql statement parameterise it and map result from execution. You don’t need to open/close connection, handle exception. 
To do this you need use add spring-jbdc jar in your class path and then create instance of JdbcTemplate and parameterise it with javax.sqlDataSource instance which need connection information in order to connect database.
Jdbc is good for small applications.

Hibernate is good sql automation. You don’t need to write sql statement and map the result. You only need define domain object and then annotate it. open hibernate transactional session from session factory do operation and close session.

Hibernate is good but has more boiler plate code like jdbc. These are opening session closing session and committing result. Spring has good alternative to it. It uses again Template design pattern so you don’t need open and close transactional session. 
You only need to define Hibernate session factory as bean and parameterise it with datasource and some properties and then you need instance of HibernateTemplate like jdbcTemplate. Spring allows to us write less code in order to use hibernate.
Hibernate is good for enterprise app which has too many tables.

  
