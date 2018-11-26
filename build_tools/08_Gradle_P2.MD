Gradle - 2 

To use gradle, firstly download gradle and copy it approciate directory and then in eclipse define new external runtime environment
To run gradle create a file named build.gradle.

Everthing in gradle are tasks. Most common plugins are java, eclipse, war
To configure project as gradle project, firstly create project as maven project then delete all maven things and libraries from build path even source directories.
If there is already a project you want to make it gradle project, project structure should be like
src
	main
		java
		resources
		webapp	
				web-inf
	test
		java

to make gradle project first configure project path if it is not standart and then
in build.gradle as follows;
	apply plugin: 'java'
	apply plugin: 'eclipse'

	defaultTasks: 'eclipse'

if you have dependencies
 	repositories{
		mavenCentral()
	}

	dependencies{ //scopes are compile, provide, runtime
		compile 'groupid:artifactid:version'
	}

to create copy task
war{
archiveName='hello_gradle.war'
webInf { from 'src/main/resources/application.xml' }
}

task deployToTomcat (type: Copy, dependsOn: 'war') {
   from war
   into 'C:\\apache-tomcat-7.0.91-windows-x64\\apache-tomcat-7.0.91\\webapps\\'
}

