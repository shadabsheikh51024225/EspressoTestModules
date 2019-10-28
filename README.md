# EspressoTestModules




Espresso is an open source android user interface (UI) testing framework developed by Google. 




Some the salient features supported by Espresso are as follow:----


Very simple API and so, easy to learn.

Highly scalable and flexible.

Provides separate module to test Android WebView component.

Provides separate module to validate as well as mock Android Intents.

Provides automatic synchronization between your application and tests.







Let us now what the benefits of Espresso are:--

Backward compatibility

Easy to setup.

Highly stable test cycle.

Supports testing activities outside application as well.

Supports JUnit4

UI automation suitable for writing black box tests.







@Test annotation

@Test -----
is the very important annotation in the JUnit framework. @Test is used to differentiate a normal method from the test case method. Once a method is decorated with @Test annotation, then that particular method is considered as a Test case and will be run by JUnit Runner.





JunitRunner class ; - 
JUnit Runner is a special class, which is used to find and run the JUnit test cases available inside the java classes. 




@After------
@After is similar to @Before, but the method annotated with @After will be called or executed after each test case is run.




@Before-----
@Before annotation is used to refer a method, which needs to be invoked before running any test method available in a particular test class.



@Rule-----
@Rule annotation is one of the highlights of JUnit. It is used to add behavior to the test cases. We can only annotate the fields of type TestRule. It actually provides feature set provided by @Before and @After annotation but in an efficient and reusable way. 







Assertion-----
Assertion is a way of checking whether the expected value of the test case matches the actual value of the test case result. JUnit provides assertion for different scenario; a few important assertions are listed below −

fail() − To explicitly make a test case fail.

assertTrue(boolean test_condition) − Checks that the test_condition is true

assertFalse(boolean test_condition) − Checks that the test_condition is false

assertEquals(expected, actual) − Checks that both values are equal

assertNull(object) − Checks that the object is null

assertNotNull(object) − Checks that the object is not null

assertSame(expected, actual) − Checks that both refers same object.

assertNotSame(expected, actual) − Checks that both refers different object.
