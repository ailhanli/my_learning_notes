There are some requirement for example transactions, security, auditing, logging. These are cross cutting concern. In OOP these leads lots of copy paste code.

Proxy pattern helps to solve this problem. Writing proxy manually is very very tedious. Java provides Dynamic Proxy, it is diffucult to use. Spring provides elegant way to solve this problem using config file a little bit. Spring Aop generates proxy for us. This is big benefit of it. Spring uses Standart jdk to easy generate proxy.

Aop Jargons
---
Aspect is requirement needs to apply in many places such as transactions, logging(for debug), security, auditing)

Advice is Main logic of aspect. it is simple code to apply. For example security auding advice. It is also known as interceptor in java world!

Weaving is simply applying advice on target code.Weaving is done in config xml file.


Advices:

Before: apply advice before target code. for example security advice. if the user login sucess then we run target code

After: runs after target code.

Around: mix of two. Advice run before target and after target. For performance monitoring we need this one. we keep before clock and after target runs clock and we look differences bw them.

For example for performance monitoring we need only write once advice and spring will weaving it!

Advice Interfaces : we need to implement these interfaces and add out payload inside them.


How to apply:

MethodBeforeAdvice(Before)
AfterReturningAdvice(After)
MethodInterceptor(Around) from aopalliance library

We need to give the bean name as in legacy code shuffle 
org.springframework.aop.framework.ProxyFactoryBean
-prop 1: proxyInterfaces (name and value is for which interface we want to create)
-prop 2: InterceptorNames(name and list of values which advice we want to use as value in list tag)
-prop 3: target (name and ref to target object which we want to wrap it)

for every bean you need to repeat xml config(weaving).  if we forget advice for example for security advice system will be unsecure. This really serious problem
Solution is aspectj pointcut syntax. It makes AOP much simpler and really powerfull.





