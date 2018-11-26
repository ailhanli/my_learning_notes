if we hardcoded create an instance of a service inside a method, it is not compile error, it is a design error. It make coupling. It is not easy to change and test it now.
In case of coupling, if the impl changed we need to recompile it and it is potentialy breaks and we need retest!

ex: lets we have a service for book and a service account. scenario is if we want to buy a book we need use firstly book service to query and then call account service to raise an invoice. In this scenario calling this all business logic inside client is not good. we need purchase service. client will only call this one no need for book and account service(facade pattern)

we normally configure service dependency value for example string, int via property value attr. for service we need use ref attr. 

for property tag
name is refer to setter method property name, value is for string or integer, ref is object.
by default spring is eagarly creates objects when container instance is created. in case we need lazyiness for performance reason we can use lazy-init attr of bean tag set true


by default all beans in container singleton and eagerly created but if you want make bean statefull you will need to change scope as prototype. Prototype beans created lazyily!! 

Constructor inject we can make via constructor-arg instead of property and we use ref tag. 
constructor injection must used in case dependency required, setter is used only dependecy is optional. constructor injection is better than setter injection because of early error thrown when container created and meaningfull error.
