Dealing Test with Legacy Code

with the mock, we create replacement of object using class name. It is a dummy object. by defaults all methods will return dummy value. We need to write stub version of what method we need. Other will still remain dummy.

We create stub version using 

when(method calling).thenReturn(value)



if a method can not be testable because of dependency, first we need to spy object and then stub the method like;

doReturn(value).(spied obj).method-call()





with spy, is ability on spying methods on a real object not a class

spy means you dont actually replace the object you still use real underlying object but you stub one or more methods

in another words, i using spying we can replace method of an object and leave the rest of the object in techt

