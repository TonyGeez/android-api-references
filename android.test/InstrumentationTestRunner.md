# InstrumentationTestRunner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstrumentationTestRunner

Kotlin| [Java](https://developer.android.com/reference/android/test/InstrumentationTestRunner "View this page in Java") 

```
open class InstrumentationTestRunner : Instrumentation, TestSuiteProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.app.Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#) ||
| | ↳ | [android.test.InstrumentationTestRunner](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#) |

| **This class was deprecated in API level 24.**
|
| Use [AndroidJUnitRunner](https://developer.android.com/reference/android/support/test/runner/AndroidJUnitRunner.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

An [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#) that runs various types of junit.framework.TestCases against an Android package (application).
|
| ### Developer Guides
|
| For more information about application testing, read the [Testing](https://developer.android.com/guide/topics/testing/index.html) developer guide.

### Typical Usage

1. Write junit.framework.TestCases that perform unit, functional, or performance tests against the classes in your package. Typically these are subclassed from:
 - [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2)
 - [android.test.ActivityUnitTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase)
 - [android.test.AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase)
 - [android.test.ApplicationTestCase](https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase)
 - [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)
 - [android.test.ProviderTestCase](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase)
 - [android.test.ServiceTestCase](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase)
 - [android.test.SingleLaunchActivityTestCase](https://developer.android.com/reference/kotlin/android/test/SingleLaunchActivityTestCase)
2. Set the`android:targetPackage`attribute of the`<instrumentation>`element in the test package's manifest. You should set the attribute value to the package name of the target application under test.
3. Run the instrumentation using "adb shell am instrument -w", with no optional arguments, to run all tests (except performance tests).
4. Run the instrumentation using "adb shell am instrument -w", with the argument '-e func true' to run all functional tests. These are tests that derive from [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase).
5. Run the instrumentation using "adb shell am instrument -w", with the argument '-e unit true' to run all unit tests. These are tests that*do not* derive from [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)(and are not performance tests).
6. Run the instrumentation using "adb shell am instrument -w", with the argument '-e class' set to run an individual junit.framework.TestCase.

<br />

<br />

**Running all tests:** adb shell am instrument -w com.android.foo/android.test.InstrumentationTestRunner

<br />

**Running all small tests:** adb shell am instrument -w -e size small com.android.foo/android.test.InstrumentationTestRunner

<br />

**Running all medium tests:** adb shell am instrument -w -e size medium com.android.foo/android.test.InstrumentationTestRunner

<br />

**Running all large tests:** adb shell am instrument -w -e size large com.android.foo/android.test.InstrumentationTestRunner

<br />

**Filter test run to tests with given annotation:** adb shell am instrument -w -e annotation com.android.foo.MyAnnotation com.android.foo/android.test.InstrumentationTestRunner

<br />

If used with other options, the resulting test run will contain the union of the two options. e.g. "-e size large -e annotation com.android.foo.MyAnnotation" will run only tests with both the [LargeTest](https://developer.android.com/reference/kotlin/android/test/suitebuilder/annotation/LargeTest) and "com.android.foo.MyAnnotation" annotations.

<br />

**Filter test run to tests*without*given annotation:** adb shell am instrument -w -e notAnnotation com.android.foo.MyAnnotation com.android.foo/android.test.InstrumentationTestRunner

<br />

**Running a single testcase:** adb shell am instrument -w -e class com.android.foo.FooTest com.android.foo/android.test.InstrumentationTestRunner

<br />

**Running a single test:** adb shell am instrument -w -e class com.android.foo.FooTest#testFoo com.android.foo/android.test.InstrumentationTestRunner

<br />

**Running multiple tests:** adb shell am instrument -w -e class com.android.foo.FooTest,com.android.foo.TooTest com.android.foo/android.test.InstrumentationTestRunner

<br />

**Running all tests in a java package:** adb shell am instrument -w -e package com.android.foo.subpkg com.android.foo/android.test.InstrumentationTestRunner

<br />

**Including performance tests:** adb shell am instrument -w -e perf true com.android.foo/android.test.InstrumentationTestRunner

<br />

**To debug your tests, set a break point in your code and pass:** -e debug true

<br />

**To run in 'log only' mode** -e log true This option will load and iterate through all test classes and methods, but will bypass actual test execution. Useful for quickly obtaining info on the tests to be executed by an instrumentation command.

<br />

**To generate EMMA code coverage:** -e coverage true Note: this requires an emma instrumented build. By default, the code coverage results file will be saved in a /data//coverage.ec file, unless overridden by coverageFile flag (see below)

<br />

**To specify EMMA code coverage results file path:** -e coverageFile /sdcard/myFile.ec 
in addition to the other arguments.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_NAME_CLASS](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_KEY_NAME_CLASS:kotlin.String) If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the name of the current test class. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_NAME_TEST](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_KEY_NAME_TEST:kotlin.String) If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the name of the current test. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_NUM_CURRENT](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_KEY_NUM_CURRENT:kotlin.String) If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the sequence number of the current test. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_NUM_TOTAL](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_KEY_NUM_TOTAL:kotlin.String) If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the total number of tests that are being run. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_STACK](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_KEY_STACK:kotlin.String) If included in the status bundle sent to an IInstrumentationWatcher, this key identifies a stack trace describing an error or failure. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_VALUE_ID](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_VALUE_ID:kotlin.String) This value, if stored with key [android.app.Instrumentation#REPORT_KEY_IDENTIFIER](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#REPORT_KEY_IDENTIFIER:kotlin.String), identifies InstrumentationTestRunner as the source of the report. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPORT_VALUE_RESULT_ERROR](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_VALUE_RESULT_ERROR:kotlin.Int) The test completed with an error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPORT_VALUE_RESULT_FAILURE](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_VALUE_RESULT_FAILURE:kotlin.Int) The test completed with a failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPORT_VALUE_RESULT_OK](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_VALUE_RESULT_OK:kotlin.Int) The test completed successfully. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPORT_VALUE_RESULT_START](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#REPORT_VALUE_RESULT_START:kotlin.Int) The test is starting. |

| Inherited constants ||
|---|---|
| From class [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#) |----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_IDENTIFIER](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#REPORT_KEY_IDENTIFIER:kotlin.String) <br /> If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the class that is writing the report. This can be used to provide more structured logging or reporting capabilities in the IInstrumentationWatcher. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_STREAMRESULT](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#REPORT_KEY_STREAMRESULT:kotlin.String) <br /> If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies a string which can simply be printed to the output stream. Using these streams provides a "pretty printer" version of the status \& final packets. Any bundles including this key should also include the complete set of raw key/value pairs, so that the instrumentation can also be launched, and results collected, by an automated system. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InstrumentationTestRunner](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#InstrumentationTestRunner())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openTestSuite! | [getAllTests](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#getAllTests())`()` Override this to define all of the tests to run in your package. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getArguments](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#getArguments())`()` Get the arguments passed to this instrumentation. |
| open [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)! | [getLoader](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#getLoader())`()` Override this to provide access to the class loader of your package. |
| openTestSuite! | [getTestSuite](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#getTestSuite())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#onCreate(android.os.Bundle))`(`arguments:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#onStart())`()` <br /> |

| Protected methods ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestListener](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#addTestListener(TestListener))`(`listener:` `TestListener!`)` Add a TestListener |
| open [AndroidTestRunner](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner)! | [getAndroidTestRunner](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner#getAndroidTestRunner())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#) |--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [TestLooperManager](https://developer.android.com/reference/kotlin/android/os/TestLooperManager.html#)! | [acquireLooperManager](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#acquireLooperManager(android.os.Looper))`(`looper:` ` [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)!`)` <br /> Takes control of the execution of messages on the specified looper until [TestLooperManager.release](https://developer.android.com/reference/kotlin/android/os/TestLooperManager.html#release())is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#addMonitor(android.app.Instrumentation.ActivityMonitor))`(`monitor:` ` [Instrumentation.ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#)!`)` <br /> Add a new [ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#) that will be checked whenever an activity is started. The monitor is added after any existing ones; the monitor will be hit only if none of the existing monitors can themselves handle the Intent. <br /> | | [Instrumentation.ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#)! | [addMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#addMonitor(android.content.IntentFilter,%20android.app.Instrumentation.ActivityResult,%20kotlin.Boolean))`(`filter:` ` [IntentFilter](https://developer.android.com/reference/kotlin/android/content/IntentFilter.html#)!`, `result:` ` [Instrumentation.ActivityResult](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityResult.html#)!`, `block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> A convenience wrapper for [addMonitor(android.app.Instrumentation.ActivityMonitor)](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#addMonitor(android.app.Instrumentation.ActivityMonitor))that creates an intent filter matching [ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#) for you and returns it. <br /> | | [Instrumentation.ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#)! | [addMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#addMonitor(kotlin.String,%20android.app.Instrumentation.ActivityResult,%20kotlin.Boolean))`(`cls:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `result:` ` [Instrumentation.ActivityResult](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityResult.html#)!`, `block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> A convenience wrapper for [addMonitor(android.app.Instrumentation.ActivityMonitor)](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#addMonitor(android.app.Instrumentation.ActivityMonitor))that creates a class matching [ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#) for you and returns it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addResults](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#addResults(android.os.Bundle))`(`results:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Report some results in the middle of instrumentation execution. Later results (including those provided by [finish](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#finish(kotlin.Int,%20android.os.Bundle))) will be combined with android.os.Bundle#putAll. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnCreate](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnCreate(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `icicle:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Perform calling of an activity's android.app.Activity#onCreate method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnCreate](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnCreate(android.app.Activity,%20android.os.Bundle,%20android.os.PersistableBundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `icicle:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `persistentState:` ` [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)!`)` <br /> Perform calling of an activity's android.app.Activity#onCreate method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnDestroy](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnDestroy(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnNewIntent](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnNewIntent(android.app.Activity,%20android.content.Intent))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` <br /> Perform calling of an activity's android.app.Activity#onNewIntent method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnNewIntent](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnNewIntent(android.app.Activity,%20android.content.Intent,%20android.app.ComponentCaller))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)`, `caller:` ` [ComponentCaller](https://developer.android.com/reference/kotlin/android/app/ComponentCaller.html#)`)` <br /> Same as [callActivityOnNewIntent(android.app.Activity,android.content.Intent)](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnNewIntent(android.app.Activity,%20android.content.Intent)), but with an extra parameter for the [ComponentCaller](https://developer.android.com/reference/kotlin/android/app/ComponentCaller.html#) instance associated with the app that sent the intent. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnPause](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnPause(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` <br /> Perform calling of an activity's [Activity.onPause](https://developer.android.com/reference/kotlin/android/app/Activity.html#onPause())method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnPictureInPictureRequested](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnPictureInPictureRequested(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)`)` <br /> Perform calling of an activity's [Activity.onPictureInPictureRequested](https://developer.android.com/reference/kotlin/android/app/Activity.html#onPictureInPictureRequested())method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnPostCreate](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnPostCreate(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> Perform calling of an activity's android.app.Activity#onPostCreate method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnPostCreate](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnPostCreate(android.app.Activity,%20android.os.Bundle,%20android.os.PersistableBundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `persistentState:` ` [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)?`)` <br /> Perform calling of an activity's android.app.Activity#onPostCreate method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnRestart](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnRestart(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` <br /> Perform calling of an activity's [Activity.onRestart](https://developer.android.com/reference/kotlin/android/app/Activity.html#onRestart())method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnRestoreInstanceState](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnRestoreInstanceState(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` <br /> Perform calling of an activity's android.app.Activity#onRestoreInstanceState method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnRestoreInstanceState](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnRestoreInstanceState(android.app.Activity,%20android.os.Bundle,%20android.os.PersistableBundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `persistentState:` ` [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)?`)` <br /> Perform calling of an activity's android.app.Activity#onRestoreInstanceState method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnResume](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnResume(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` <br /> Perform calling of an activity's [Activity.onResume](https://developer.android.com/reference/kotlin/android/app/Activity.html#onResume())method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnSaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnSaveInstanceState(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)`, `outState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` <br /> Perform calling of an activity's android.app.Activity#onSaveInstanceState method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnSaveInstanceState](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnSaveInstanceState(android.app.Activity,%20android.os.Bundle,%20android.os.PersistableBundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)`, `outState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`, `outPersistentState:` ` [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)`)` <br /> Perform calling of an activity's android.app.Activity#onSaveInstanceState method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnStart](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnStart(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` <br /> Perform calling of an activity's [Activity.onStart](https://developer.android.com/reference/kotlin/android/app/Activity.html#onStart())method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnStop](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnStop(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` <br /> Perform calling of an activity's [Activity.onStop](https://developer.android.com/reference/kotlin/android/app/Activity.html#onStop())method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnUserLeaving](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callActivityOnUserLeaving(android.app.Activity))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` <br /> Perform calling of an activity's [Activity.onUserLeaveHint](https://developer.android.com/reference/kotlin/android/app/Activity.html#onUserLeaveHint())method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callApplicationOnCreate](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#callApplicationOnCreate(android.app.Application))`(`app:` ` [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)!`)` <br /> Perform calling of the application's [Application.onCreate](https://developer.android.com/reference/kotlin/android/app/Application.html#onCreate())method. The default implementation simply calls through to that method. Note: This method will be called immediately after [onCreate(android.os.Bundle)](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#onCreate(android.os.Bundle)). Often instrumentation tests start their test thread in onCreate(); you need to be careful of races between these. (Well between it and everything else, but let's start here.) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [checkMonitorHit](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#checkMonitorHit(android.app.Instrumentation.ActivityMonitor,%20kotlin.Int))`(`monitor:` ` [Instrumentation.ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#)!`, `minHits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Test whether an existing [ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#) has been hit. If the monitor has been hit at least minHits times, then it will be removed from the activity monitor list and true returned. Otherwise it is left as-is and false is returned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endPerformanceSnapshot](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#endPerformanceSnapshot())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#finish(kotlin.Int,%20android.os.Bundle))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `results:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Terminate instrumentation of the application. This will cause the application process to exit, removing this instrumentation from the next time the application is started. If multiple processes are currently running for this instrumentation, all of those processes will be killed. <br /> | | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getAllocCounts](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getAllocCounts())`()` <br /> Returns a bundle with the current results from the allocation counting. <br /> | | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getBinderCounts](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getBinderCounts())`()` <br /> Returns a bundle with the counts for various binder counts for this process. Currently the only two that are reported are the number of send and the number of received transactions. <br /> | | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)! | [getComponentName](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getComponentName())`()` <br /> Returns complete component name of this instrumentation. <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getContext](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getContext())`()` <br /> Return the Context of this instrumentation's package. Note that this is often different than the Context of the application being instrumentated, since the instrumentation code often lives is a different package than that of the application it is running against. See [getTargetContext](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getTargetContext())to retrieve a Context for the target application. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProcessName](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getProcessName())`()` <br /> Return the name of the process this instrumentation is running in. Note this should only be used for testing and debugging. If you are thinking about using this to, for example, conditionalize what is initialized in an Application class, it is strongly recommended to instead use lazy initialization (such as a getter for the state that only creates it when requested). This can greatly reduce the work your process does when created for secondary things, such as to receive a broadcast. <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getTargetContext](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getTargetContext())`()` <br /> Return a Context for the target application being instrumented. Note that this is often different than the Context of the instrumentation code, since the instrumentation code often lives is a different package than that of the application it is running against. See [getContext](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getContext())to retrieve a Context for the instrumentation code. <br /> | | [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#)! | [getUiAutomation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getUiAutomation())`()` <br /> Gets the [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) instance with no flags set. **Note:** The APIs exposed via the returned [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) work across application boundaries while the APIs exposed by the instrumentation do not. For example, [Instrumentation.sendPointerSync(MotionEvent)](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendPointerSync(android.view.MotionEvent))will not allow you to inject the event in an app different from the instrumentation target, while [UiAutomation.injectInputEvent(android.view.InputEvent, boolean)](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#injectInputEvent(android.view.InputEvent,%20kotlin.Boolean))will work regardless of the current application. A typical test case should be using either the [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) or [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#) APIs. Using both APIs at the same time is not a mistake by itself but a client has to be aware of the APIs limitations. Equivalent to`getUiAutomation(0)`. If a [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) exists with different flags, the flags on that instance will be changed, and then it will be returned. Compatibility mode: This method is infallible for apps targeted for [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) and earlier versions; for apps targeted for later versions, it will return null if [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) fails to connect. The caller can check the return value and retry on error. <br /> | | [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#)! | [getUiAutomation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getUiAutomation(kotlin.Int))`(`flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) instance with flags set. **Note:** The APIs exposed via the returned [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) work across application boundaries while the APIs exposed by the instrumentation do not. For example, [Instrumentation.sendPointerSync(MotionEvent)](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendPointerSync(android.view.MotionEvent))will not allow you to inject the event in an app different from the instrumentation target, while [UiAutomation.injectInputEvent(android.view.InputEvent, boolean)](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#injectInputEvent(android.view.InputEvent,%20kotlin.Boolean))will work regardless of the current application. A typical test case should be using either the [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) or [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#) APIs. Using both APIs at the same time is not a mistake by itself but a client has to be aware of the APIs limitations. If a [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) exists with different flags, the flags on that instance will be changed, and then it will be returned. Compatibility mode: This method is infallible for apps targeted for [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) and earlier versions; for apps targeted for later versions, it will return null if [UiAutomation](https://developer.android.com/reference/kotlin/android/app/UiAutomation.html#) fails to connect. The caller can check the return value and retry on error. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [invokeContextMenuAction](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#invokeContextMenuAction(android.app.Activity,%20kotlin.Int,%20kotlin.Int))`(`targetActivity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Show the context menu for the currently focused view and executes a particular context menu item. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [invokeMenuActionSync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#invokeMenuActionSync(android.app.Activity,%20kotlin.Int,%20kotlin.Int))`(`targetActivity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Execute a particular menu item. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProfiling](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#isProfiling())`()` <br /> Check whether this instrumentation was started with profiling enabled. <br /> | | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)! | [newActivity](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#newActivity(java.lang.Class,%20android.content.Context,%20android.os.IBinder,%20android.app.Application,%20android.content.Intent,%20android.content.pm.ActivityInfo,%20kotlin.CharSequence,%20android.app.Activity,%20kotlin.String,%20kotlin.Any))`(`clazz:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `token:` ` [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)!`, `application:` ` [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `info:` ` [ActivityInfo](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `parent:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `lastNonConfigurationInstance:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Perform instantiation of an [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) object. This method is intended for use with unit tests, such as android.test.ActivityUnitTestCase. The activity will be useable locally but will be missing some of the linkages necessary for use within the system. <br /> | | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)! | [newActivity](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#newActivity(java.lang.ClassLoader,%20kotlin.String,%20android.content.Intent))`(`cl:` ` [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` <br /> Perform instantiation of the process's [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) object. The default implementation provides the normal system behavior. <br /> | | [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)! | [newApplication](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#newApplication(java.lang.ClassLoader,%20kotlin.String,%20android.content.Context))`(`cl:` ` [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> Perform instantiation of the process's [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#) object. The default implementation provides the normal system behavior. <br /> | | [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)! | [newApplication](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#newApplication(java.lang.Class,%20android.content.Context))`(`clazz:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> Perform instantiation of the process's [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#) object. The default implementation provides the normal system behavior. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroy](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#onDestroy())`()` <br /> Called when the instrumented application is stopping, after all of the normal application cleanup has occurred. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onException](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#onException(kotlin.Any,%20kotlin.Throwable))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> This is called whenever the system captures an unhandled exception that was thrown by the application. The default implementation simply returns false, allowing normal system handling of the exception to take place. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#removeMonitor(android.app.Instrumentation.ActivityMonitor))`(`monitor:` ` [Instrumentation.ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#)!`)` <br /> Remove an [ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#) that was previously added with #addMonitor. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetInTouchMode](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#resetInTouchMode())`()` <br /> Resets the [touch mode](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#setInTouchMode(kotlin.Boolean))to the device default. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runOnMainSync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#runOnMainSync(java.lang.Runnable))`(`runner:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Execute a call on the application's main thread, blocking until it is complete. Useful for doing things that are not thread-safe, such as looking at or modifying the view hierarchy. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendCharacterSync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendCharacterSync(kotlin.Int))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends up and down key events with the given key code to the currently focused window, and waits for it to be processed. Equivalent to [sendKeyDownUpSync(int)](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendKeyDownUpSync(kotlin.Int)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeyDownUpSync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendKeyDownUpSync(kotlin.Int))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends up and down key events with the given key code to the currently focused window, and waits for it to be processed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeySync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendKeySync(android.view.KeyEvent))`(`event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Sends a key event to the currently focused window, and waits for it to be processed. This method blocks until the recipient has finished handling the event. Note that the recipient may*not*have completely finished reacting from the event when this method returns. For example, it may still be in the process of updating its display or UI contents upon reacting to the injected event. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendPointerSync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendPointerSync(android.view.MotionEvent))`(`event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> Dispatches a pointer event into a window owned by the instrumented application, and waits for it to be processed. If the motion event being injected is targeted at a window that is not owned by the instrumented application, the input injection will fail. See [getUiAutomation()](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#getUiAutomation())for injecting events into all windows. This method blocks until the recipient has finished handling the event. Note that the recipient may*not*have completely finished reacting from the event when this method returns. For example, it may still be in the process of updating its display or UI contents upon reacting to the injected event. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendStatus](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendStatus(kotlin.Int,%20android.os.Bundle))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `results:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Provide a status report about the application. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendStringSync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendStringSync(kotlin.String))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends the key events that result in the given text being typed into the currently focused window, and waits for it to be processed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendTrackballEventSync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#sendTrackballEventSync(android.view.MotionEvent))`(`event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> Dispatches a trackball event into the currently focused window, and waits for it to be processed. This method blocks until the recipient has finished handling the event. Note that the recipient may*not*have completely finished reacting from the event when this method returns. For example, it may still be in the process of updating its display or UI contents upon reacting to the injected event. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutomaticPerformanceSnapshots](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#setAutomaticPerformanceSnapshots())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInTouchMode](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#setInTouchMode(kotlin.Boolean))`(`inTouch:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Force the global system in or out of touch mode. This can be used if your instrumentation relies on the UI being in one more or the other when it starts. **Note:** Starting from Android [Build.VERSION_CODES.TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int), this method will only take effect if the instrumentation was sourced from a process with`MODIFY_TOUCH_MODE_STATE`internal permission granted (shell already have it). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#start())`()` <br /> Create and start a new thread in which to run instrumentation. This new thread will call to [onStart](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#onStart())where you can implement the instrumentation. <br /> | | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)! | [startActivitySync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#startActivitySync(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` <br /> Start a new activity and wait for it to begin running before returning. In addition to being synchronous, this method as some semantic differences from the standard android.content.Context#startActivity call: the activity component is resolved before talking with the activity manager (its class name is specified in the Intent that this method ultimately starts), and it does not allow you to start activities that run in a different process. In addition, if the given Intent resolves to multiple activities, instead of displaying a dialog for the user to select an activity, an exception will be thrown. The function returns as soon as the activity goes idle following the call to its android.app.Activity#onCreate. Generally this means it has gone through the full initialization including [Activity.onResume](https://developer.android.com/reference/kotlin/android/app/Activity.html#onResume())and drawn and displayed its initial window. <br /> | | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) | [startActivitySync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#startActivitySync(android.content.Intent,%20android.os.Bundle))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` <br /> Start a new activity and wait for it to begin running before returning. In addition to being synchronous, this method as some semantic differences from the standard android.content.Context#startActivity call: the activity component is resolved before talking with the activity manager (its class name is specified in the Intent that this method ultimately starts), and it does not allow you to start activities that run in a different process. In addition, if the given Intent resolves to multiple activities, instead of displaying a dialog for the user to select an activity, an exception will be thrown. The function returns as soon as the activity goes idle following the call to its android.app.Activity#onCreate. Generally this means it has gone through the full initialization including [Activity.onResume](https://developer.android.com/reference/kotlin/android/app/Activity.html#onResume())and drawn and displayed its initial window. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAllocCounting](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#startAllocCounting())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPerformanceSnapshot](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#startPerformanceSnapshot())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startProfiling](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#startProfiling())`()` <br /> This method will start profiling if isProfiling() returns true. You should only call this method if you set the handleProfiling attribute in the manifest file for this Instrumentation to true. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopAllocCounting](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#stopAllocCounting())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopProfiling](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#stopProfiling())`()` <br /> Stops profiling if isProfiling() returns true. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [waitForIdle](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#waitForIdle(java.lang.Runnable))`(`recipient:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Schedule a callback for when the application's main thread goes idle (has no more events to process). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [waitForIdleSync](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#waitForIdleSync())`()` <br /> Synchronously wait for the application to be idle. Can not be called from the main application thread -- use [start](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#start())to execute instrumentation in its own thread. <br /> | | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)! | [waitForMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#waitForMonitor(android.app.Instrumentation.ActivityMonitor))`(`monitor:` ` [Instrumentation.ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#)!`)` <br /> Wait for an existing [ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#) to be hit. Once the monitor has been hit, it is removed from the activity monitor list and the first created Activity object that matched it is returned. <br /> | | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)! | [waitForMonitorWithTimeout](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#waitForMonitorWithTimeout(android.app.Instrumentation.ActivityMonitor,%20kotlin.Long))`(`monitor:` ` [Instrumentation.ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#)!`, `timeOut:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Wait for an existing [ActivityMonitor](https://developer.android.com/reference/kotlin/android/app/Instrumentation.ActivityMonitor.html#) to be hit till the timeout expires. Once the monitor has been hit, it is removed from the activity monitor list and the first created Activity object that matched it is returned. If the timeout expires, a null object is returned. <br /> | ||

## Constants

### REPORT_KEY_NAME_CLASS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_KEY_NAME_CLASS: String
```

**Deprecated:** *Deprecated in Java.*

If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the name of the current test class. This is sent with any status message describing a specific test being started or completed. 

 Value: "class"

### REPORT_KEY_NAME_TEST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_KEY_NAME_TEST: String
```

**Deprecated:** *Deprecated in Java.*

If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the name of the current test. This is sent with any status message describing a specific test being started or completed. 

 Value: "test"

### REPORT_KEY_NUM_CURRENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_KEY_NUM_CURRENT: String
```

**Deprecated:** *Deprecated in Java.*

If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the sequence number of the current test. This is sent with any status message describing a specific test being started or completed. 

 Value: "current"

### REPORT_KEY_NUM_TOTAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_KEY_NUM_TOTAL: String
```

**Deprecated:** *Deprecated in Java.*

If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the total number of tests that are being run. This is sent with all status messages. 

 Value: "numtests"

### REPORT_KEY_STACK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_KEY_STACK: String
```

**Deprecated:** *Deprecated in Java.*

If included in the status bundle sent to an IInstrumentationWatcher, this key identifies a stack trace describing an error or failure. This is sent with any status message describing a specific test being completed. 

 Value: "stack"

### REPORT_VALUE_ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_VALUE_ID: String
```

**Deprecated:** *Deprecated in Java.*

This value, if stored with key [android.app.Instrumentation#REPORT_KEY_IDENTIFIER](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#REPORT_KEY_IDENTIFIER:kotlin.String), identifies InstrumentationTestRunner as the source of the report. This is sent with all status messages. 

 Value: "InstrumentationTestRunner"

### REPORT_VALUE_RESULT_ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_VALUE_RESULT_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

The test completed with an error. 

 Value: -1

### REPORT_VALUE_RESULT_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_VALUE_RESULT_FAILURE: Int
```

**Deprecated:** *Deprecated in Java.*

The test completed with a failure. 

 Value: -2

### REPORT_VALUE_RESULT_OK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_VALUE_RESULT_OK: Int
```

**Deprecated:** *Deprecated in Java.*

The test completed successfully. 

 Value: 0

### REPORT_VALUE_RESULT_START

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REPORT_VALUE_RESULT_START: Int
```

**Deprecated:** *Deprecated in Java.*

The test is starting. 

 Value: 1

## Public constructors

### InstrumentationTestRunner

```
InstrumentationTestRunner()
```

## Public methods

### getAllTests

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllTests(): TestSuite!
```

**Deprecated:** *Deprecated in Java.*

Override this to define all of the tests to run in your package. 

### getArguments

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getArguments(): Bundle!
```

**Deprecated:** *Deprecated in Java.*

Get the arguments passed to this instrumentation.

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | the Bundle object |

### getLoader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLoader(): ClassLoader!
```

**Deprecated:** *Deprecated in Java.*

Override this to provide access to the class loader of your package. 

### getTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTestSuite(): TestSuite!
```

**Deprecated:** *Deprecated in Java.* 

### onCreate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreate(arguments: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `arguments` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Any additional arguments that were supplied when the instrumentation was started. |

### onStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStart(): Unit
```

**Deprecated:** *Deprecated in Java.*

## Protected methods

### addTestListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun addTestListener(listener: TestListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Add a TestListener 

### getAndroidTestRunner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getAndroidTestRunner(): AndroidTestRunner!
```

**Deprecated:** *Deprecated in Java.*
