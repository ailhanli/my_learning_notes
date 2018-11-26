Spring xml config is good and readable. Time by time it will be too big. We can separate in many files.
From beginning of the Spring there is bean parameter which “autowire" can be used. It does magic wire 
required property or constructor parameter behind the scene. 
byName: simply looks up in xml for property set without set
byType: simply looks up by type in xml for property 
constructor: simply looks up by type in xml for constructor
example: <bean id=“aa” class=“asd” autowire=“byType”/>

We can use annotation approach. Simply add @Component at the class level for all beans 
and add  <context:component-scan base-package="com.vpp.chp18”/> in example base package is 
for where to scan for annotations.

StereoType annotations: These are marker annotations. Nothing different on their functionality
@Component: general purpose
@Service: for service layer. business logic layer
@Repository: for dao layer. data logic layer

@Autowire wires beans. It can be used on Constructor, Setter or Fields
Constructor injection should use for required beans.
Setter for optional. 
Fields not recommended. Because it makes class bean tightly coupled. Not good for test.

In annotation driven approach. Many magics done behind the scene.

On note that DataSource, JdbcTemplate, DataSourceTransactionManager cannot be scan by context:component-scan
these are from spring jar files and they need as single instance. They can not autowire and need to define by ourself.

@Component on this time spring create bean by className in camel case
otherwise you can use as @Component (“service”). It is good idea.




