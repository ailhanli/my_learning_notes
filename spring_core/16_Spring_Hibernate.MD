Spring Hibernate Integratiton Notes

Hibernate is a sql automation framework. You dont need to right sql scripts and also mapping resultset. 
In default hibernate implementation, there are several things we have to talk about. 
- config file: this is for hibernate framework configuration like Spring
- we need to session before every transaction and need to close session after it
- Typical hibernate orm bean should start with @Entity and have @Id column for identification inside hibernate

Default implemantiton is boiler plate codes(tedious and repetitive code). you need create session open session execute method and then close session. In spring integration you dont need to do this

Hibernate has sql style language which is diffucult to learn but easy to use.
It is simplified version of SQL. 

In Spring integration simply we need to define sessionfactory in xml and put datasource, packagesToScan property
We also need Hibernate Transaction manager instead of jdbc version.

Spring manages hibernate session factory lifecycle. 


