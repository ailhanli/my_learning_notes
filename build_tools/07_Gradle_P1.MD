Gradle - 1

Gradle is combination of maven and ant good features.

- Everything in gradle is task. Task is same as ant target and can be depend on each other. You can define new tasks also. 
- Gradle has good plugins and we can use tasks under the these plugins. This behaviour is same as maven behaviour.

What we have faced using ant and gradle?

In ant everything should be written by developer explicitly and if you want run same  target again you have to explicitly copy paste it with different name. You cant loop it. 
Maven is better than ant but everything in maven are plugins. You can use lifecycle but if you need more specific plugin you have write own. One bad things that everthing in both tools must be written in xml. Xml is good for keeping data within tag but not good for logic. 


Gradle uses groovy lang so you write groovy script inside it. for instance you can run your tests in the midnight build using if statement.



