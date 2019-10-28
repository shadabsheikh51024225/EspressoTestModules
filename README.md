# EspressoTestModules




Espresso is an open source android user interface (UI) testing framework developed by Google. 




Some the salient features supported by Espresso are as follow:----


Very simple API and so, easy to learn.

Highly scalable and flexible.

Provides separate module to test Android WebView component.

Provides separate module to validate as well as mock Android Intents.

Provides automatic synchronization between your application and tests.


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------














Let us now what the benefits of Espresso are:--

Backward compatibility

Easy to setup.

Highly stable test cycle.

Supports testing activities outside application as well.

Supports JUnit4

UI automation suitable for writing black box tests.



--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------













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










--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------







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



--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------







Espresso provides a large number of classes to test user interface and the user interaction of an android application. They can be grouped into five categories as specified below −






JUnit runner
Android testing framework provides a runner, AndroidJUnitRunner to run the espresso test cases written in JUnit3 and JUnit4 style test cases. It is specific to android application and it transparently handles loading the espresso test cases and the application under test both in actual device or emulator, execute the test cases and report the result of the test cases. To use AndroidJUnitRunner in the test case, we need to annotate the test class using @RunWith annotation and then pass the AndroidJUnitRunner argument as specified below −

@RunWith(AndroidJUnit4.class)
   public class ExampleInstrumentedTest {
}
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





JUnit rules
Android testing framework provides a rule, ActivityTestRule to launch an android activity before executing the test cases. It launches the activity before each method annotated with @Test` and @Before. It will terminate the activity after method annotated with @After. A sample code is as follows,

@Rule
public ActivityTestRule<MainActivity> mActivityTestRule = new ActivityTestRule<>(MainActivity.class);

Here, MainActivity is the activity to be launched before running a test case and destroyed after the particular test case is run.


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

ViewMatchers---

Espresso provides large number of view matcher classes (in androidx.test.espresso.matcher.ViewMatchers package) to match and find UI elements / views in an android activity screen’s view hierarchy. Espresso’s method onView takes a single argument of type Matcher (View matchers), finds the corresponding UI view and returns corresponding ViewInteraction object. ViewInteraction object returned by onView method can be further used to invoke actions like click on the matched view or can be used to assert the matched view


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


ViewActions
Espresso provides large number of view action classes (in androidx.test.espresso.action.ViewActions) to invoke the different action on the selected / matched view. Once onView matches and returns ViewInteraction object, any action can be invoked by calling “perform” method of ViewInteraction object and pass it with proper view actions. A sample code to click the matched view is as follows,

ViewInteraction viewInteraction = Espresso.onView(withText("Hello World!"));
viewInteraction.perform(click());
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

ViewAssertions
Similar to view matchers and view actions, Espresso provides a large number of view assertion (in androidx.test.espresso.assertion.ViewAssertions package) to assert the matched view is what we expected. Once onView matches and returns the ViewInteraction object, any assert can be checked using check method of ViewInteraction by passing it with proper view assertion. A sample code to assert that the matched view is as follows,

ViewInteraction viewInteraction = Espresso.onView(withText("Hello World!"));
viewInteraction.check(matches(withId(R.id.text_view)));

Here, matches accept the view matcher and return view assertion, which can be checked by check method of ViewInteraction.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------







