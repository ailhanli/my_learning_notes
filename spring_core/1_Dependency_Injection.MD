It is a fundamental principle of Spring Framework.

Simply, a software has many classes. We create many classes to adhere SRP. A class has an Interface. Two classes must be interact each other via their Interface and they don’t need to know each other. 

We generally create a class instance(object) in another class constructor, method or field. In case we create an instance in these places using new operator we create tightly coupled system. Aim of Spring dependency injection is simply manage these dependencies(configure and create an object) smoothly via configuration and make classes testable and we can change easily implementation. We create loosely coupled system.



Coupling: If a class dependent to another class, they are coupled. if one changed other will be changed also. There are some problems here:

1- Managing changes

2- Testing

1- For small program coupling is doesn’t matter. For enterprise app, if one class changes, all the place where changes class used will be change and need re-test.

2- We can’t test classes because it depends another. It is not a single unit. Unit test should be faster and safe. If a class dependent to DAO class, it will be slow and database will be pollute and in case changes to DB will be risky.



Coupling is nature. Without coupling you can’t use one class inside another. Goal is reducing coupling.

We can talk coupling on enterprise side. if one layer changed, we won’t change another. 



TO solve coupling;

1- Program to interface

2- Dependency injection

3- Centralised configuration



Spring does all of it via container.



Dependency Injection is giving collaborators via parameters rather than hard coding. Using New keyword inside a class make coupling is hard. 

The main purpose is testing in isolation. If we use dependency injection we isolate layers and we don’t touch already tested classes. But it is not enough and we can’t feel comfortable!



Hard coding dependency injection is not good as centralized injection. Every time you need to give dependency etc.



Two ways dependency injection is common: Setter and constructor injection but we can do also it by field via container. Setter injection without container make class in invalid state!



Centralized configuration means move all configuration on place to manage easily. But moving in java class, it will be very big and need recompile in case of any changes Thats why we need vendor containers and use simple configuration file to easily manage configuration. Container is configuration manager. it creates and configure objects. Pico, GUICE and Spring are common containers but Spring can do more than being container!



spesification means interface!

