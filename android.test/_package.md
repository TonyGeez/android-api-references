# android.test

# android.test

Kotlin| [Java](../android/test/_package.md)
| --- | --- |

## Interfaces

| [PerformanceTestCase](../android/test/PerformanceTestCase.md) | More complex interface performance for test cases. |
| --- | --- |
| [TestSuiteProvider](../android/test/TestSuiteProvider.md) | Implementors will know how to get a test suite. |

## Classes

| [ActivityInstrumentationTestCase](../android/test/ActivityInstrumentationTestCase.md) | This class provides functional testing of a single activity. |
| --- | --- |
| [ActivityInstrumentationTestCase2](../android/test/ActivityInstrumentationTestCase2.md) | This class provides functional testing of a single activity. |
| [ActivityTestCase](../android/test/ActivityTestCase.md) | This is common code used to support Activity test cases. |
| [ActivityUnitTestCase](../android/test/ActivityUnitTestCase.md) | This class provides isolated testing of a single activity. |
| --- | --- |
| [AndroidTestCase](../android/test/AndroidTestCase.md) | Extend this if you need to access Resources or other things that depend on Activity Context. |
| [AndroidTestRunner](../android/test/AndroidTestRunner.md) | <br /> |
| [ApplicationTestCase](../android/test/ApplicationTestCase.md) | This test case provides a framework in which you can test Application classes in a controlled environment. |
| --- | --- |
| [InstrumentationTestCase](../android/test/InstrumentationTestCase.md) | A test case that has access to [Instrumentation](../android/app/Instrumentation.md). |
| [InstrumentationTestRunner](../android/test/InstrumentationTestRunner.md) | An [Instrumentation](../android/app/Instrumentation.md) that runs various types of junit. |
| [InstrumentationTestSuite](../android/test/InstrumentationTestSuite.md) | A junit. |
| --- | --- |
| [IsolatedContext](../android/test/IsolatedContext.md) | A mock context which prevents its users from talking to the rest of the device while stubbing enough methods to satify code that tries to talk to other packages. |
| [LaunchPerformanceBase](../android/test/LaunchPerformanceBase.md) | Base class for all launch performance Instrumentation classes. |
| [LoaderTestCase](../android/test/LoaderTestCase.md) | A convenience class for testing [Loader](../android/content/Loader.md) s. |
| --- | --- |
| [MoreAsserts](../android/test/MoreAsserts.md) | Contains additional assertion methods not found in JUnit. |
| [ProviderTestCase](../android/test/ProviderTestCase.md) | If you would like to test a single content provider with an [InstrumentationTestCase](../android/test/InstrumentationTestCase.md), this provides some of the boiler plate in [setUp](../android/test/ProviderTestCase.md))and [tearDown](../android/test/ProviderTestCase.md)). |
| [ProviderTestCase2](../android/test/ProviderTestCase2.md) | This test case class provides a framework for testing a single [ContentProvider](../android/content/ContentProvider.md) and for testing your app code with an isolated content provider. |
| --- | --- |
| [RenamingDelegatingContext](../android/test/RenamingDelegatingContext.md) | This is a class which delegates to the given context, but performs database and file operations with a renamed database/file name (prefixes default names with a given prefix). |
| [ServiceTestCase](../android/test/ServiceTestCase.md) | This test case provides a framework in which you can test Service classes in a controlled environment. |
| [SingleLaunchActivityTestCase](../android/test/SingleLaunchActivityTestCase.md) | If you would like to test a single activity with an [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md), this provides some of the boiler plate to launch and finish the activity in [setUp](../android/test/SingleLaunchActivityTestCase.md))and [tearDown](../android/test/SingleLaunchActivityTestCase.md)). |
| --- | --- |
| [SyncBaseInstrumentation](../android/test/SyncBaseInstrumentation.md) | If you would like to test sync a single provider with an [InstrumentationTestCase](../android/test/InstrumentationTestCase.md), this provides some of the boiler plate in [setUp](../android/test/SyncBaseInstrumentation.md))and [tearDown](../android/test/InstrumentationTestCase.md)). |
| [TouchUtils](../android/test/TouchUtils.md) | Reusable methods for generating touch events. |
| [ViewAsserts](../android/test/ViewAsserts.md) | Some useful assertions about views. |
| --- | --- |

## Exceptions

| [AssertionFailedError](../android/test/AssertionFailedError.md) | Thrown when an assertion failed. |
| --- | --- |
| [ComparisonFailure](../android/test/ComparisonFailure.md) | Thrown when an assert equals for Strings failed. |

## Annotations

| [FlakyTest](../android/test/FlakyTest.md) | This annotation can be used on an [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md)'s test methods. |
| --- | --- |
| [RepetitiveTest](../android/test/RepetitiveTest.md) | This annotation can be used on an [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md)'s test methods. |
| [UiThreadTest](../android/test/UiThreadTest.md) | This annotation can be used on an [InstrumentationTestCase](../android/test/InstrumentationTestCase.md)'s test methods. |
