Advance topic in TDD 2



Mockito is replacement for a class dependency. By default it created dummy implementation of class and the  we can implement it as write what do to when specific method called. This is known as stubbing



So far we write test for data. Value of sone objects matches what we expected.

But sometimes we need if a method is called or not which is testing behaviour. Did a code behaves what we expected. Did a method we expected to run actually run or Did a method we expected to not run ,not runs. We tested code flow here not just get right value out.



Mockito is used by default for this and it is good for also data testing. with mockito we can create data driven test easy than test stub