Hello everyone, welcome to functional programming training. Before the training I would like ask who has been experience functional programming before? Great! 

Before I started, I want to inform that I wont talk details in deep about functional programming. That’s because we don’t have enough time. I will try to explain concept behind the scene. Actually, you dont need to know Java. Basic programming knowledge is enough.



Motivation
------------------------------------
<b>Assembly</b> is a programming language for writing program for microprocessor and devices. Even for simple looping you have to write lots of instructions. It is good for hardware not for business.

<b>Procedural languages</b> are good for writing simple business software. For example PL/SQL. What we do that we develop our business inside procedures. We write lots of procedure and call them in order to do our business. Drawbacks are it is not easy to extend and do maintenance. 

<b>Object oriented programming</b> is new way of modeling real world business applications in terms of objects

SOLID is important principle for writing object oriented program

S for Single Responsibility, class should be change for only one reason

O for open for extension close for modification, check decorator and strategy pattern

L is liskow principle subclass should be substitutable for base class, avoiding inheritance 

I is interface segregation it is actually single responsibility in terms of interfaces, so interface should be small as small possible

D is dependency inversion which means classes should talk each other in terms of abstractions

If you are not using SOLID principle, you are actually writing Object Based Programming. With OOP, you can easy to maintain and extend the code. Drawback is writing multithreaded program is really hard.

<b>Functional programming</b> is different than all others. You can write more readable, maintainable, extendable code than OOP. Concurreny is really easier than all others.
Functional code is smaller than procedural and uses object oriented programming principle behind the scene. Drawback is it is diffucult concept to understand and i will explain sharp corner of this new paradigm.



What is function
--------------------------------------
<b> F(x) = x+1 </b>

In mathematic; function can defined fx= x+1 simply. What it means that for every x, result should be x+1. If result is different than x+1 it is not pure function we can say function has side effect. Mathematical functions are pure functions. Programming function depends.



Side effect
----------------------------------------
Side effects can be happen during the all kind of IO operations including reading/writing from/to file, reading/writing from/to database, calling web service etc..

For instance if file is deleted your program can throw an exception or if database is changed by third party, result will can be invalid so we can say result is not x+1.



What is functional programming
--------------------------------------
Simply functions as a first class citizens. what it means that you can assign function to a variable, send to a method as a parameter or return from method. method is simply procedure in Java.




In Java
-------------------------------------
Lambda expression is fundamental of functional programming. The term comes from Lambda calculus. Lambda is a implementation of functional interface in Java. Functional interface is an interface which has single method only.

What is an interface? Interface is simply a contract between caller and callee.

Java has several built-in functional interfaces. 
How can we read interfaces? We have to focus on What this interface takes and returns. 

For example Consumer interface take any type of parameter and return nothing so it consumes 
or Function interface take any type of parameter return different types.



Declarative versus imperative programming mode
----------------------------------------
In imperative programming model, we simply say what and how to do business logic. In declarative programming model, we only say what to do! Programming language will do job for us. We will see how can we write declarative program on next topic.



When we can use lambda expression in our code?
----------------------------------------
Lambda expression is simply an anonymous method which is a method has no names:) when we have different type of algorithms and we want to change our algorithm without changing our main functionality, we can use lambda. This is actually strategy design pattern.

Because lambda is strategy pattern we can change it at runtime. Lambda is implementation of functional interface. So it is lazy. When interface method is called lambda will execute.

Lets try 
practice 1: practice fundamental of functional programming 
practice 2: lazy execution



Metaphor
--------------------------------------
Almost in all programs we use mostly collections. We iterate collection via iterator pattern and do some calculation. iterator pattern is a pattern which traverse to collection.

Java has Stream API which an API uses iterator and recursion. with stream API, we write our program uses sql like operators. All operators take lambda expression as a parameter.

It has three types of component: source, intermediate and terminal. 
- Source can be collections, array, file..etc
- intermediate operator can be filter, map, sort, distinct 
- terminal operators can be collect, toArray, count, reduce
If chain hasnt terminator, it wont be execute. So it is lazy. lets try! lets do more example and understand how can we program functional uses stream api.

practice 3 : finding maximum numbers between 1 to 100 which divide by 10. --first look at lazy execution --first do it in procedural way then functional

practice 4: finding total salary of employee which has same age

practice 5: show example of city pair used by tap project. first explain problem and then solution.

practice 6: show example of campaingn management code. first explain problem and then solution.

practice 7: make parallel



In legacy code
--------------------------------------
For the old projects which has been developed in earlier version of Java for example Java 7 or before. we can't use it. If our project in java 8, we can write some parts especially, doing business with collection using java 8 or at least we can write our daily external things in java 8 as i did. It is also a first step for learning reactive which will me presented in next week.



Drawbacks
------------------------------------
For collection related jobs, functional programming is good but performance is not better than classic looping structure sometimes. or other things, which are mostly has many details we cannot write functional.

Practice 8: show one example..Hello everyone, welcome to functional programming training. Before the training I would like ask who has been experience functional programming before? Great!, 

Before I started, I want to inform that I wont talk details in deep about functional programming. That’s because we don’t have enough time. I will try to explain concept behind the scene. Actually, you dont need to know Java. Basic programming knowledge is enough.

