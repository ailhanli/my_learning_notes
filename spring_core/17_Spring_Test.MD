Spring Integratition Test

The test for the layers called integratition test.

**Manuel test is really bad and slow. Everytime you use your eyes and sometimes you miss result. We need one button to click every test runs!

Test includes three stages:
arrange: in this phase we need create require data
act: run aspect we want to test
assert: assert result

@Test: needed on the top of every test method. test method should be meaningfull.
@Test(expected=Exception.class): in this case we dont need to write any assert because exception will be caught by the JUnit
@Before: will run before every test.

If we create for example Spring container inside @Before method it will be create container every time will included the time of test. It will slow the tests if hundreads of method to be tested.
If we create it inside constructor, constructor will run before all test methods. Junit wants to make garbage all data after end of test. Thats because construction will not included inside time of test but it is incorrect.

Defining data inside each method separately insulated all methods from each other. Thats good. Thats for the find method we need to insert first then search it. For the insert we need insert at least two record and then check if it is inserted corretly maybe via number of records check

Spring has couple of annotations for the integratition test:
@RunWith(SpringJunit4ClassRunner.class)
@ContextConfiguration("/application.properties")
It will provide one container for all tests.

The problem is when we runs test if the class changes database, test will fails sometimes. It is incrediably terible.
We need to add @Annotational on top of Test. It is different than we see before. It start a begin transaction and end of method it will rollback it. It makes test methods isolated from each other.

Integratition test can run on db and it wont work time by time because of db changes stayed after every test