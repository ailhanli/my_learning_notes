Advance Topic in Test-1



Lets talk about  a bit what kind of problems we can face in case of dependency. It is actually common thing



if a test has a dependency, it can be database or web service. so we don’t want to test external and we want to test only our business logic but we have some problems in our test these are

if external system is down, our test wont work
if data is changed on external system or new data come test wont repeatable.
so that’s why we need to isolate our test from dependency.



How can we do. 

We can create test stub to solve this problem. Test stub is mockup implementation of external system. When we can able to create stub

external service should implement an interface
interface should be small


otherwise we need third party library.

