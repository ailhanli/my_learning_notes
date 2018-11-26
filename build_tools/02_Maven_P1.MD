Maven  Part-1

Maven means expert in a field. Maven is expert in a build. 
In ant you have explain everything  and do a lot of jobs.You have to define directories and your build step by step it is tedious. 

Maven is sophicticated and knows how to build. You have say a little about your project. if you need war file you say generate war file. rather than saying how to build step by step.
- low configuration building: it handles relatively low configuration. 
- dependency management: instead of download and use jar. you only says what you need. maven finds jars automatically.
- consistent project layout: most projects has exactly same layout. rather than inventing own convention. it is very good if you move project to project.
WHY maven. because you dont need to define all low level thing in detail. maven can do for you automatically. dependency managment is also more easy than ant only declare what you depends on.

Project_Name
-src
       -test: test source files
       -main
                          -resources: configurations
                          -webapp:any files for web
                          -java:source code
pom.xml: key maven file

pom is project object model.
pom doesnt have any logic. it is simply a configuration of project. It only has set of declaration about high level structure of project. there is no directory in pom. thats because maven knows how to compile

- project: in contains namespace in order to validate pom.
- modelversion: maven version
- groupid: name of the company who owns. it reverse domain name of company and uniquely identifier project
- artifactid: project name
- version: version of app
- packaging: take parameter as jar for pck
dependencies: project depends upon external libraries. maven find download and install jar file or combination of them.
scope of dependency for example test says that this jar only needed to run test. in case of packaging maven wont add it inside package.

combination of groupid and artifactid globally uniquelly identify project

for the first time compile project, maven needs internet connection. 
by default maven cant even compile. everthing can do via plugins. this plugin download by maven from maven central repository to cache for the first time. on the next run plugin will run from cache.
remember that even for the simple operation for example delete dir is done via plugin. you dont need define anything. maven will find and install them when first run from central repository.
sometimes you got connection error during the download. so wait few minutes and try again. sometime maven central so busy.

to compile project, select second configurable build and add to goal compile command. goal is same as ant target.

maven compile
