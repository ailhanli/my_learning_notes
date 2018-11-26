AspectJ

It is really powerfull. We can apply many classes or some methods inside a class which are impossible with old way
This syntax is borrowed from Aspectj. Thats why we need to add jar file for aspectj. But we are not using all the feature of it

Pointcut is a set of rules determining to which methods and in which class a piece of advice should be applied.
for example: all methods beginning with 'get' in all service classes
*Service*.get*
using aspectj we will use crosscutting objects for better modularity
pointcut syntax is wildcard syntax. Spring barrows this syntax from aspectj and observed it spring fw. it is actually nothing more than wildcard.
we wont use aspectj. but we will use pointcut syntax which is borrowed from aspectj

*Service*.*get(String,*): all service classes get method which first param is String and second param is any type and must have second param

*Service*.*get*(..): all service classes get methods with zero or more params, '..' means we dont care about number of parameters and their types

List *Service*.*get(..): same as before except must return List of any type

You must always have return type reference in point cut syntax. point cut expression should be in execution().

execution(List *Service*.*get(..)): all get method execution inside all service class has one or more params and returns List.


How to Apply
In Spring 2, We don’t need to implement any interface. These has advantages. We don’t need to remember interfaces to implement.Method we called write we can call anything we want. And we don’t need to write new classes for all different version for example timing advice. We just add new method for all variations. It is valuable. We can group related methods in single class. 
For Around advice we need a single parameter ProceedingJoinPoint class variable.

