Maven Part-4

when you import a maven project. Maybe it cant be compiled. So you have to run maven eclipse:eclipse plugin or simply right click update maven project.

In maven app there are three sections
section 1 is project info definition
section 2 is dependency definition
section 3 is plugin configuration if needed

dependencies has three things we have to define.
groupid which is project owner
artifactid which is project name
version which is version of app
the artifactid and groupid combination should be unique.

Scopes:
compile: jar will be used on both compile and runtime and will be in package
provided: jar should be provided by it user. mostly used for app server which has already jar
test: jar will used by test and it wont import into package
runtime: jar only be used at runtime

if we need package for the project we need to define what kind of packaging like 
<packaging> war </packaging>

Plugin is simply maven jar developed by maven developers.
in order to create package correctly we need to configure packaging plugin.
for the standalone app, we have to configure assembly plugin, for the war war plugin should be configured.
for more information checkup github page.  https://github.com/superdevelopertr/build_tools_by_vpp_maven

All maven project pom.xml is extended from super pom which is built in pom and contains maven address and all default configurations. 
We can override default behaviour in our pom file. (http://maven.apache.org/plugins/) 
<build>
	<plugins>
		<plugin>
			<groupid></groupid>
			<artifactid></artifactid>
			<version></version>
			<configurations>
				inside here you can override default.
			</configurations>
			<executions>
				inside here you can add your goal end of any phase
			</executions>
		<plugin>
	<plugins>
</build>




