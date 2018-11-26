We create business logic on service layer and delegate persistence to dao layer. We program to interface(spesification)

Some requirement needs in many places but they are not related place where they applies, this is known as Aspect, we can not easily apply aspect with OOP, we need to program AOP

sampleaspexf is timing
With OOP,
Same aspect is many places which is known as code scattering, in this case changing aspect code require changes in many places and it is awfull. Aspect is not related to a class functionality where it apply, it violates SRP. it is not requirement for particulat class or method. For example timing every method in service class. we can measure timing in case jdbc or hibernate. PMP happy with it but we are not:) Every time we add method we need to add timing. Code repeation!!! or if we need to change timing logic. if we need to disable aspect, we need if statement also. it is not easy to apply to on all classes

oop is all about creating class defining behaviour via set of methods. aspects is more than it. we need apply it in every places maybe

first solution is proxy. proxy solves srp problems and it is bot easy to write for hundreads of methods. you still have code repation. Java has solution which is called dynamic proxy. You provide payload it generates proxy for all hundreads of methods. but you dont need know how it works. spring do easyliy via config. 