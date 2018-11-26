TDD important notes



UNIT TEST

because you write unit test, we can feel free to refactor code and add new method. In case of wrongly changed code test will fails. maintenance and adding new feature is easy. It is better than manual test. in manual test, may you know api wrong or you loose problematic case. 





WHAT IS TDD:

test first program later in order to see what is in your mind.

three steps to follow;

red: test should fails first. if not fails, may something goes wrong. we write test for outcomes without prejudge design
green: write minimum code to pass test
refactor: finally optimise code and test




WHAT MAKES TEST GOOD

test method should cover only one piece of logic. it can be multiple assert inside test method for same logic too see logic behaviour for different inputs
write test for logic not for method. Because we write test first, we see what are in our mind to complete this job
test should be repeatable and consistent. this is very important rule. for example if a test case give input new date for job scheduling system will fails for some cases. it shouldn’t be run only for last run. It should be give same result for every run!!!
all logic should be covered in test class. but in test method only one logic should be covered




LOGiC

true cases: for example isbn number calculation result should be divided by 11 successfully
fail cases: this is opposite of true cases: if result cannot be divided by 11 it should fails
edge cases: this is edge case of test: for example isbn number last digit can be x, and for x value add 10 to sum
error cases: invalid isbn length, non numeric isbn number


Bad example: measuring performance of method cannot be a part of TDD.Thats Because it is not repeatable and has dependency to environment.


