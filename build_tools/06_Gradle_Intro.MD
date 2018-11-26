Gradle

Gradle place ant and maven and combine together.
Grade uses programming language instead xml configuration file. Language is called Groovy
If you know groovy you can do advance stuff. 
Gradle has a concept calls tasks which are different than ant tasks. That is big confusing we saw how to program tasks.
You can manipulate task it is impossible in ant.

Ant is oldest build tool. Maven is much more sophisticated and it is also fairly complicated i thing  you need good grade of lifecycle and plugins to work with maven. And as you pom get little bit complicated. 
Gradle is much newer build tool. Generally it copies best feature of  ants and maven and same time add much more power what is keeping build scripts small and simple as well. It is  not widely use as maven and ant. 

Big deal out grade is it doesn’t use xml for its configuration.Problem with xml is really it is really just a collection of tags and values and that might me ok holding properties storing information about things but it is absolutely useless to do any programming. of course it is. xml is not a programming language. That something you need to create build and put some logic in build thats after all why we call them build scripts.

Let say you repeat the tasks 5 times. doing this in ant really hard. there is no easy way defining logic and loops. Maven is same really. Maven hides complexity via plugins. if you want to do sophistical  things in maven like some logic you have write own your plugin with the logic inside the plugin. Gradle completely has different approach.

Build scripts in grade is is code proper first class programming language.Anything you do in program code you can do in grade build. Grade scripts are regulate programs which means we get a lot more powerfull  but in grade you haven’t use the java writing the scripts. 
gradle scripts are written in a programming language called Groovy.Groovy runs on JVM. That means it can interoperate in java well
for most purposes, you don’t need to learn Groovy. Thats because Groovy is really flexible language. What the grade people done is that taken a language a changed around a lot to make it look like we can write build scripts even realising programming. Which is known as DSL. Domain Specific Language.
Gradle scripts doesn’t look like xml  or program code. one of big feature of groovy is that you can twisted bend which around make it look completely different programming language  

Groovy task is equivalent to ant target which is known as grouping ant tasks. In order to use Groovy tasks we have to use plugins.
For example java plugins has everything we need in order to build-test-package out java program.

Gradle script is a program script you can do anything that you could doing in code. Thats something really impossible in ant.
You can define task. You can add java or groovy code inside task.  You can manipulate tasks. You can change dependecies on the fly that might be you do often. it great to know you can do it in gradle. 

Gradle do most of hard work via plugin. Gradle is bit like maven in this respect. With few lines of  groovy we will able to use java plugin to compile all of our code.When you want to deploy, you need another plugin which is war plugin. Because jars are stored in hidden directory,  If you want code compile under the eclipse we going to update build path somehow in eclipse 