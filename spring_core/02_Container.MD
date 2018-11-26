Spring container is centralized dependency injection container. It is ioc container. Every object inside container name as bean.

Spring container in traditional way work with xml configuration. In case application configuration change you dont need to recompile classes if you use xml configuration.

Client ask to container for beans via interface. Container looks xml file to create beans and then inject dependency. After that return instance of bean.

You need XmlConfigurationApplicationContext class instance to access container.

You can set dependency via property. If it is an array of string for example, you need to set property via list attr.

How to?
You defined bean inside beans tag if necessary with id in case there are more than one implementations and inject dependecy via property tag.
If there are more than on customer requested different impl you can create xml per customer.

xml configuration file is a wiring classes place. We wire beans via this file. 
In case we need time to develop a service we can create mock version(fake object which has hard coded data) of this service for reseolving dependency problem with client. So client can develop without exact service. in xml file you can easliy change beans without recompile client code or any layer in multi tier app.

xml vs annotation driven concept: in annotaition driven it will be default to change implementation class. In xml version it is more readable but take time to write and will be big for real projects you have split it in several files.
