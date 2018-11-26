Spring Pointcut More

<aop:config>
	<aop:aspect ref=“”>
		<aop:around method=“” pointcut=“”/>
	</aop:aspect>
</aop:config>

to define this tag we have to add document type definition(dtd) on xml.
it basically point a file on springframework.org. That files define what is valid in xml.
it actually stores in jar having your lib directory. This is old way fashion. Xml committee define new xml validation which is called xmlschema. it has same job as dtd but lot more flexible and useful. Spring 2 developer use schema to validate tags. dtd version is deprecated and less important. You have to stop to use dtd. For this course we will use dtd. 

this new syntax dramatically cut xml syntax we used before. it is compact readable and understandable syntax.

Using annotations for aop is not recommended. Annotation is for for other things we will do.
For use annotation you need to add to config file <aop:aspectj-autoproxy/>
And then you have to add @Aspect annotation on top of class, spring will recognize this is an advise class. 
In case you use annotation for AOP and if changes require or disabling needed you have recompile and aspect class will be complicated.