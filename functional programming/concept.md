
Hello everyone, welcome to functional programming training. 
Before training I would like ask who has been experience functional programming before?
Great!, before I started, I want to inform that I wont talk details in deep about functional programming. That’s because we don’t have enough time. I will try to explain concept behind the scene. Actually, you dont need to know java. Basic programming knowledge is enough.





motivation
------------------------------------

Assembly was first programming language. it is for writing program for microprocessor and devices. 
Even for simple looping you have to write lots of instructions.

Procedural languages are good for writing simple business software. for example pl/sql. what we do in procedural.
we writes lots of procedure and call them in order to do job. drawbacks are it is not easy to extend and do maintenance.

Object oriented programming is new way of modeling real world business applications in terms of objects. if you are not 
using SOLID principle, you are actually writing object oriented style procedural programming. benefits are more maintainable
and easy to extendable code. drawback is writing concurrent program is really hard.

Functional programming is different than all others before. you can write more readable, maintainable, extendable code. 
concurrent is really easier than all others.

Functional code is smaller than procedural and uses object oriented programming principle behind the scene
drawback is it is not easy to undestand new way of thinking which functional programming and i will explain sharp corner of 
this new paradigm.





what is function
--------------------------------------
In mathematic function is fx= x+1 simply. what it means. for every x, result should be x+1. if result is different than x+1
it is not pure function we can say function has side effect. Mathematical function is pure function. Programming function is depends.

Side effects in programming are all kind of io operations including reading from file, writing to database, calling web service etc..

When you do io during the function execution, function result can be different. for instance if file is deleted or data is 
changed by third party, your program can throw an exception so we can say result is not x+1.




definition
--------------------------------------
It is simple functions as a first class citizens. what it means? it means you can assign function to a variable, send to a method as a parameter or return from method. method is simply procedure in java.




in java
-------------------------------------
lambda expression is fundamental of functional of programming. Lambda is a implementation of functional interface.
functional interface is an interface which has single method only. 

What is an interface? interface is simply a contract between caller and callee. 

Java has several built-in functional interfaces. the main concern should be when reading an interface. what this interface takes and returns.
For example Consumer interface take any type of parameter and return nothing. so it consumes.
or Function interface take any type of parameter return different types.




declarative versus imperative programming mode
----------------------------------------
In imperative programming model, we simply say what and how to do using conditional statements, looping statements.
In declarative programming model, we only say what to do, programming language will do job for us. We will see how can we write declarative program on next topic.



when we can use lambda expression in our code?
----------------------------------------
Lambda expression is simply an anonymous method which is a method has no names:)
when we have different type of algorithm and we change it without changing our main method, we can use lambda.
This is actually strategy design pattern. 

Because lambda is strategy pattern we can change it at runtime. 
lambda is simply functional interface. so it is lazy. when interface method is called lambda will execute.

lets try

practice 1: practice fundamental of functional programming




metaphor
--------------------------------------
Almost in our all program we use mostly collections. We iterate collection via iterator pattern and do some calculation.
iterator pattern is a pattern which traverse to collection.

Java has stream api which an api uses iterator and recursion. with stream api, we write our program uses sql like operators.
all operators take lambda expression as a parameter.

It has three components: source, intermediate operators and terminators.
source can be collection, array or file
intermediate operator can be filter, map, sort, distinct
terminator can be collect, toArray, count, reduce

If chain hasnt terminator, it wont be execute. so it is lazy. lets try!
lets do more example and understand how can we program functional uses stream api.
example 2 : finding maximum numbers between 1 to 100 which divide by 10. 
--first look at lazy execution
--first do it in procedural way then functional
example 3: finding total salary of employee which has same age

example 4: show example of city pair used by tap project. first explain problem and then solution.
example 5: show example of campaingn management code. first explain problem and then solution.
example 6: make parallel



in legacy code
--------------------------------------
For the old projects which has been developed in earlier version of java for example java 7 or before. we can't use it.
if our project in java 8, we can write some parts especially, doing business with collection using java 8. 
or at least we can write our daily external things in java 8 as i did. 
it is also a first step for learning reactive which will me presented in next week.



drawbacks
------------------------------------
For collection related jobs, functional programming is good but performance is not better than classic looping structure
sometimes. or other things, which are mostly has many details we cannot write functional.

example: show one example..

