Build Scripts: Ant

**define how can you read ant doc
**comment one fully tasks and then paste it as sample notes about ant.

purpose is automate build-runtest-javadoc…etc
It consists several tasks.

Task is small job ANT can do.
Tasks are not production standard. It is monolithic. i mean there is no modularity and flexibility.

Target is group of tasks together. It is actually one or more group of tasks.
Target can be small or big it depends on project. In many projects target is small. Each task is target.
Tasks are predefined by ANT. We invoke task using it xml tag.
We create out own named targets.

When we using ant do different things than task. 
We can select which target we run by eclipse run configuration or defined at beginning of project tag using default property of it.

--Dependency—
Target can depends upon each other. We can do it by using depends property of each target.
There are two approaches to run:
Approach 1: define a target make it default ant set it dependencies in order.
Approach 2: make a target default then make chain of dependencies. it has advantage. if we decided to change run target which we want on run configuration, dependency will still remain on new one.

for example running cleaning target before compile target is very important. thats why they depends each other. we all make sure correct steps have been followed first.


