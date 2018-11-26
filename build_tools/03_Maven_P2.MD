Maven Part-2

Our pom should be declaring which are the important project to our project if you use them directly in our code then i would strongly consider adding it to the pom even if i acquired it transitive dependency.

what is transactive dependency?
There are two types of dependecy. first one is direct dependency which is directly declare in our project's pom file. 
transactive one is a dependecy which is dependecy of direct dependency. it is actually indirect dependency.
In case we need to use directive dependency in our project directly, we have to define it as direct dependency in the pom file.

Scopes: 
There are several scopes we can define. But all have different purpose.
compile: this is a by default scope. it means that dependency will used both on compile and runtime and will be in package.
test: this means that this dependency only will be used for test and wont be exported in package
provided: this simply means that i am using this dependency in the project for both compile and runtime but it wont be included inside package. it will be provided by runtime environment. if we use a dependency and it has provided dependency we have to provide it otherwise we cant compile out project.

Optional: it means that depency is an optional dependency. it only will be used to compile project and wont be used for runtime.

Versions: version is important. most project used fixed version. if we change version we have to check first backward compability. spring is a big project so it is trully backward compatible. 
we can define range for version.
[1.0,2.0] we will use latest one included 2.0
[1.0,2.0) we will use latest before 2.0
LATEST: it means get latest one from maven central repo
RELEASE: get latest production standart version from central repo.


When we compile project using maven compile. all dependency will be downloaded on our cache. whihc is .m2 directory on user home directory. Sometime we can get classnot found exception even we have dependency. first we need to check jar file if exist under the .m2 directory. if not delete simply .m2 directory and recompile project.

You can analysize pom file of dependency in order to check all it's dependencies.


