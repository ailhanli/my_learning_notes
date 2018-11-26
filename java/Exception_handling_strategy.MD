exception handling

statement which throw check exception should be in try and we have to provide catch block. or we we can propogate exception to caller.
for example sqlexception says something go wrong on database maybe query maybe database down etc

inside catch block only logging case of for example table is already exist. sqlexception is too general. if the network is down it goes wrong. we print table is already created but false that could result really bad things happen

unchecked exception is an exception it can be catched optionally and control is down on our program.

spring categorizes sqlexception and you do t need to handle excpetion in try catch exception special cases required. in special cases we use spesific exception. if we use sqlexception we will double up every possible problems


if we are not using app server we can use apache common dbcp. if we use, we need jndi.

if we write an application using jndi in standart jee way our code will be app server dependent code and cant run without app server.  and it is boiler plate code

one of big advantage of spring is you can run your code either on app server or it can be basic console app via xml configuration

best way is start with console app, if you need advance feature of app server or it is politic decision you can change it as jndi. for this purpose please create different xml. so you can run your code without app server if you are hurry and need to fast debug.



