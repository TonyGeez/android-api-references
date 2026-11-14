# android.test

# android.test

Kotlin| [Java](https://developer.android.com/reference/android/test/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [PerformanceTestCase](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase) | More complex interface performance for test cases. |
| --- | --- |
| [TestSuiteProvider](https://developer.android.com/reference/kotlin/android/test/TestSuiteProvider) | Implementors will know how to get a test suite. |

## Classes

| [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) | This class provides functional testing of a single activity. |
| --- | --- |
| [ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2) | This class provides functional testing of a single activity. |
| [ActivityTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase) | This is common code used to support Activity test cases. |
| [ActivityUnitTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase) | This class provides isolated testing of a single activity. |
| --- | --- |
| [AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase) | Extend this if you need to access Resources or other things that depend on Activity Context. |
| [AndroidTestRunner](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner) | <br /> |
| [ApplicationTestCase](https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase) | This test case provides a framework in which you can test Application classes in a controlled environment. |
| --- | --- |
| [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) | A test case that has access to [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#). |
| [InstrumentationTestRunner](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner) | An [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#) that runs various types of junit. |
| [InstrumentationTestSuite](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestSuite) | A junit. |
| --- | --- |
| [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext) | A mock context which prevents its users from talking to the rest of the device while stubbing enough methods to satify code that tries to talk to other packages. |
| [LaunchPerformanceBase](https://developer.android.com/reference/kotlin/android/test/LaunchPerformanceBase) | Base class for all launch performance Instrumentation classes. |
| [LoaderTestCase](https://developer.android.com/reference/kotlin/android/test/LoaderTestCase) | A convenience class for testing [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#) s. |
| --- | --- |
| [MoreAsserts](https://developer.android.com/reference/kotlin/android/test/MoreAsserts) | Contains additional assertion methods not found in JUnit. |
| [ProviderTestCase](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase) | If you would like to test a single content provider with an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase), this provides some of the boiler plate in [setUp](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#setUp())and [tearDown](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#tearDown()). |
| [ProviderTestCase2](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2) | This test case class provides a framework for testing a single [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#) and for testing your app code with an isolated content provider. |
| --- | --- |
| [RenamingDelegatingContext](https://developer.android.com/reference/kotlin/android/test/RenamingDelegatingContext) | This is a class which delegates to the given context, but performs database and file operations with a renamed database/file name (prefixes default names with a given prefix). |
| [ServiceTestCase](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase) | This test case provides a framework in which you can test Service classes in a controlled environment. |
| [SingleLaunchActivityTestCase](https://developer.android.com/reference/kotlin/android/test/SingleLaunchActivityTestCase) | If you would like to test a single activity with an [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase), this provides some of the boiler plate to launch and finish the activity in [setUp](https://developer.android.com/reference/kotlin/android/test/SingleLaunchActivityTestCase#setUp())and [tearDown](https://developer.android.com/reference/kotlin/android/test/SingleLaunchActivityTestCase#tearDown()). |
| --- | --- |
| [SyncBaseInstrumentation](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation) | If you would like to test sync a single provider with an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase), this provides some of the boiler plate in [setUp](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation#setUp())and [tearDown](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#tearDown()). |
| [TouchUtils](https://developer.android.com/reference/kotlin/android/test/TouchUtils) | Reusable methods for generating touch events. |
| [ViewAsserts](https://developer.android.com/reference/kotlin/android/test/ViewAsserts) | Some useful assertions about views. |
| --- | --- |

## Exceptions

| [AssertionFailedError](https://developer.android.com/reference/kotlin/android/test/AssertionFailedError) | Thrown when an assertion failed. |
| --- | --- |
| [ComparisonFailure](https://developer.android.com/reference/kotlin/android/test/ComparisonFailure) | Thrown when an assert equals for Strings failed. |

## Annotations

| [FlakyTest](https://developer.android.com/reference/kotlin/android/test/FlakyTest) | This annotation can be used on an [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)'s test methods. |
| --- | --- |
| [RepetitiveTest](https://developer.android.com/reference/kotlin/android/test/RepetitiveTest) | This annotation can be used on an [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)'s test methods. |
| [UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest) | This annotation can be used on an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)'s test methods. |
