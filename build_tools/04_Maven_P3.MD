Maven Part -3

Everthing in maven are plugins. for example in order to compile source files you use compiler plugin even to delete directory you use plugin. 
If you want to interesting things, you have to use plugin. There are hundreds of plunging you can use.
visit maven.apache.org/plugins

You don’t need to install plugin yourself. Maven can do for you on first use automatically download and use it. 

Each plugin has goals which are the job of plugin can do.
for example: 
compiler has two goals. first one is compile another one is testCompile. 
compiler:compile: compiles source codes and generate binary class files.
compiler:testCompile: compiles test codes and generate binary class for test cases.

if we want to do something different than plugin does as standard, we have to configure it implicitly in pom file. for example:
<build>

	<plugins>
		<plugin>
			<artifactId>maven-compiler-plugin</artifactId>

			<version>3.7.0</version>

			<configuration>

				<verbose>true</verbose>

			<configuration>

		</plugin>
	</plugins>
</build>
 


—plugin—
maven plugins are actaully maven jar. It is downloaded when first time use by maven automatically. 

compiler: compile
compiler is plugin name
compile is goal

if you want configure plugin override some properties. add it inside pom.xml plugins section and then overide plugin configuration which is after groupid/artifactid/version

calling sequence of plugin is actually tedious it is something like ant literature
we dont usually need run serious of tedious plugins.

—lifecycle—-
maven lifecycle is a serious of phases and each phase been step in a build. by default three built in lifecycle. interesting one is default lifecycle.

what exactly happen in each phases. well intention is each of these phases is a kind of generic step. and we can slot into any of these phases any goal we want to execute. and also if we want we can leave phase empty. 
maven designer setup some more important phases for us. 
each phases call related plugin if it is already setup.

if you run any phase, all phases before these will be executed
if you run compiler:compile; it is single goal running
if compile : you run compile phase of default lifecycle.
if we call package phase, maven will run all phases before package and package phase finally.

other lifecycles are clean and site.
clean for simply delete target.
site for create site for your project but it needs plugin configuration for better web site.