# android.test

# android.test

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [PerformanceTestCase](PerformanceTestCase.md) | More complex interface performance for test cases. |
| --- | --- |
| [TestSuiteProvider](TestSuiteProvider.md) | Implementors will know how to get a test suite. |

## Classes

| [ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md) | This class provides functional testing of a single activity. |
| --- | --- |
| [ActivityInstrumentationTestCase2](ActivityInstrumentationTestCase2.md) | This class provides functional testing of a single activity. |
| [ActivityTestCase](ActivityTestCase.md) | This is common code used to support Activity test cases. |
| [ActivityUnitTestCase](ActivityUnitTestCase.md) | This class provides isolated testing of a single activity. |
| --- | --- |
| [AndroidTestCase](AndroidTestCase.md) | Extend this if you need to access Resources or other things that depend on Activity Context. |
| [AndroidTestRunner](AndroidTestRunner.md) | <br /> |
| [ApplicationTestCase](ApplicationTestCase.md) | This test case provides a framework in which you can test Application classes in a controlled environment. |
| --- | --- |
| [InstrumentationTestCase](InstrumentationTestCase.md) | A test case that has access to [Instrumentation](../android.app/Instrumentation.md). |
| [InstrumentationTestRunner](InstrumentationTestRunner.md) | An [Instrumentation](../android.app/Instrumentation.md) that runs various types of junit. |
| [InstrumentationTestSuite](InstrumentationTestSuite.md) | A junit. |
| --- | --- |
| [IsolatedContext](IsolatedContext.md) | A mock context which prevents its users from talking to the rest of the device while stubbing enough methods to satify code that tries to talk to other packages. |
| [LaunchPerformanceBase](LaunchPerformanceBase.md) | Base class for all launch performance Instrumentation classes. |
| [LoaderTestCase](LoaderTestCase.md) | A convenience class for testing [Loader](../android.content/Loader.md) s. |
| --- | --- |
| [MoreAsserts](MoreAsserts.md) | Contains additional assertion methods not found in JUnit. |
| [ProviderTestCase](ProviderTestCase.md) | If you would like to test a single content provider with an [InstrumentationTestCase](InstrumentationTestCase.md), this provides some of the boiler plate in [setUp](ProviderTestCase.md))and [tearDown](ProviderTestCase.md)). |
| [ProviderTestCase2](ProviderTestCase2.md) | This test case class provides a framework for testing a single [ContentProvider](../android.content/ContentProvider.md) and for testing your app code with an isolated content provider. |
| --- | --- |
| [RenamingDelegatingContext](RenamingDelegatingContext.md) | This is a class which delegates to the given context, but performs database and file operations with a renamed database/file name (prefixes default names with a given prefix). |
| [ServiceTestCase](ServiceTestCase.md) | This test case provides a framework in which you can test Service classes in a controlled environment. |
| [SingleLaunchActivityTestCase](SingleLaunchActivityTestCase.md) | If you would like to test a single activity with an [android.test.InstrumentationTestCase](InstrumentationTestCase.md), this provides some of the boiler plate to launch and finish the activity in [setUp](SingleLaunchActivityTestCase.md))and [tearDown](SingleLaunchActivityTestCase.md)). |
| --- | --- |
| [SyncBaseInstrumentation](SyncBaseInstrumentation.md) | If you would like to test sync a single provider with an [InstrumentationTestCase](InstrumentationTestCase.md), this provides some of the boiler plate in [setUp](SyncBaseInstrumentation.md))and [tearDown](InstrumentationTestCase.md)). |
| [TouchUtils](TouchUtils.md) | Reusable methods for generating touch events. |
| [ViewAsserts](ViewAsserts.md) | Some useful assertions about views. |
| --- | --- |

## Exceptions

| [AssertionFailedError](AssertionFailedError.md) | Thrown when an assertion failed. |
| --- | --- |
| [ComparisonFailure](ComparisonFailure.md) | Thrown when an assert equals for Strings failed. |

## Annotations

| [FlakyTest](FlakyTest.md) | This annotation can be used on an [android.test.InstrumentationTestCase](InstrumentationTestCase.md)'s test methods. |
| --- | --- |
| [RepetitiveTest](RepetitiveTest.md) | This annotation can be used on an [android.test.InstrumentationTestCase](InstrumentationTestCase.md)'s test methods. |
| [UiThreadTest](UiThreadTest.md) | This annotation can be used on an [InstrumentationTestCase](InstrumentationTestCase.md)'s test methods. |
