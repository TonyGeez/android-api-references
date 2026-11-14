# InstrumentationTestRunner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstrumentationTestRunner

Kotlin| [Java](../android/test/InstrumentationTestRunner.md) 
| --- | --- |

```
open class InstrumentationTestRunner : Instrumentation, TestSuiteProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.app.Instrumentation](../android/app/Instrumentation.md) ||
| | ↳ | [android.test.InstrumentationTestRunner](../android/test/InstrumentationTestRunner.md) |

| **This class was deprecated in API level 24.**
|
| Use [AndroidJUnitRunner](../android/support/test/runner/AndroidJUnitRunner.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

An [Instrumentation](../android/app/Instrumentation.md) that runs various types of junit.framework.TestCases against an Android package (application).
|
| ### Developer Guides
|
| For more information about application testing, read the [Testing](https://developer.android.com/guide/topics/testing/index.html) developer guide.

### Typical Usage

1. Write junit.framework.TestCases that perform unit, functional, or performance tests against the classes in your package. Typically these are subclassed from:
 - [android.test.ActivityInstrumentationTestCase2](../android/test/ActivityInstrumentationTestCase2.md)
 - [android.test.ActivityUnitTestCase](../android/test/ActivityUnitTestCase.md)
 - [android.test.AndroidTestCase](../android/test/AndroidTestCase.md)
 - [android.test.ApplicationTestCase](../android/test/ApplicationTestCase.md)
 - [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md)
 - [android.test.ProviderTestCase](../android/test/ProviderTestCase.md)
 - [android.test.ServiceTestCase](../android/test/ServiceTestCase.md)
 - [android.test.SingleLaunchActivityTestCase](../android/test/SingleLaunchActivityTestCase.md)
2. Set the`android:targetPackage`attribute of the`<instrumentation>`element in the test package's manifest. You should set the attribute value to the package name of the target application under test.
3. Run the instrumentation using "adb shell am instrument -w", with no optional arguments, to run all tests (except performance tests).
4. Run the instrumentation using "adb shell am instrument -w", with the argument '-e func true' to run all functional tests. These are tests that derive from [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md).
5. Run the instrumentation using "adb shell am instrument -w", with the argument '-e unit true' to run all unit tests. These are tests that*do not* derive from [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md)(and are not performance tests).
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

If used with other options, the resulting test run will contain the union of the two options. e.g. "-e size large -e annotation com.android.foo.MyAnnotation" will run only tests with both the [LargeTest](../android/test/suitebuilder/annotation/LargeTest.md) and "com.android.foo.MyAnnotation" annotations.

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
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_NAME_CLASS](../android/test/InstrumentationTestRunner.md) If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the name of the current test class. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_NAME_TEST](../android/test/InstrumentationTestRunner.md) If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the name of the current test. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_NUM_CURRENT](../android/test/InstrumentationTestRunner.md) If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the sequence number of the current test. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_NUM_TOTAL](../android/test/InstrumentationTestRunner.md) If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the total number of tests that are being run. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_STACK](../android/test/InstrumentationTestRunner.md) If included in the status bundle sent to an IInstrumentationWatcher, this key identifies a stack trace describing an error or failure. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_VALUE_ID](../android/test/InstrumentationTestRunner.md) This value, if stored with key [android.app.Instrumentation#REPORT_KEY_IDENTIFIER](../android/app/Instrumentation.md), identifies InstrumentationTestRunner as the source of the report. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPORT_VALUE_RESULT_ERROR](../android/test/InstrumentationTestRunner.md) The test completed with an error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPORT_VALUE_RESULT_FAILURE](../android/test/InstrumentationTestRunner.md) The test completed with a failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPORT_VALUE_RESULT_OK](../android/test/InstrumentationTestRunner.md) The test completed successfully. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REPORT_VALUE_RESULT_START](../android/test/InstrumentationTestRunner.md) The test is starting. |

| Inherited constants ||
|---|---|
| From class [Instrumentation](../android/app/Instrumentation.md) |----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_IDENTIFIER](../android/app/Instrumentation.md) <br /> If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies the class that is writing the report. This can be used to provide more structured logging or reporting capabilities in the IInstrumentationWatcher. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [REPORT_KEY_STREAMRESULT](../android/app/Instrumentation.md) <br /> If included in the status or final bundle sent to an IInstrumentationWatcher, this key identifies a string which can simply be printed to the output stream. Using these streams provides a "pretty printer" version of the status \& final packets. Any bundles including this key should also include the complete set of raw key/value pairs, so that the instrumentation can also be launched, and results collected, by an automated system. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InstrumentationTestRunner](../android/test/InstrumentationTestRunner.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openTestSuite! | [getAllTests](../android/test/InstrumentationTestRunner.md))`()` Override this to define all of the tests to run in your package. |
| open [Bundle](../android/os/Bundle.md)! | [getArguments](../android/test/InstrumentationTestRunner.md))`()` Get the arguments passed to this instrumentation. |
| open [ClassLoader](../java/lang/ClassLoader.md)! | [getLoader](../android/test/InstrumentationTestRunner.md))`()` Override this to provide access to the class loader of your package. |
| --- | --- |
| openTestSuite! | [getTestSuite](../android/test/InstrumentationTestRunner.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreate](../android/test/InstrumentationTestRunner.md))`(`arguments:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](../android/test/InstrumentationTestRunner.md))`()` <br /> |
| --- | --- |

| Protected methods ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestListener](../android/test/InstrumentationTestRunner.md))`(`listener:` `TestListener!`)` Add a TestListener |
| open [AndroidTestRunner](../android/test/AndroidTestRunner.md)! | [getAndroidTestRunner](../android/test/InstrumentationTestRunner.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [Instrumentation](../android/app/Instrumentation.md) |--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [TestLooperManager](../android/os/TestLooperManager.md)! | [acquireLooperManager](../android/app/Instrumentation.md))`(`looper:` ` [Looper](../android/os/Looper.md)!`)` <br /> Takes control of the execution of messages on the specified looper until [TestLooperManager.release](../android/os/TestLooperManager.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addMonitor](../android/app/Instrumentation.md))`(`monitor:` ` [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!`)` <br /> Add a new [ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md) that will be checked whenever an activity is started. The monitor is added after any existing ones; the monitor will be hit only if none of the existing monitors can themselves handle the Intent. <br /> | | [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)! | [addMonitor](../android/app/Instrumentation.md))`(`filter:` ` [IntentFilter](../android/content/IntentFilter.md)!`, `result:` ` [Instrumentation.ActivityResult](../android/app/Instrumentation.ActivityResult.md)!`, `block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> A convenience wrapper for [addMonitor(android.app.Instrumentation.ActivityMonitor)](../android/app/Instrumentation.md))that creates an intent filter matching [ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md) for you and returns it. <br /> | | [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)! | [addMonitor](../android/app/Instrumentation.md))`(`cls:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `result:` ` [Instrumentation.ActivityResult](../android/app/Instrumentation.ActivityResult.md)!`, `block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> A convenience wrapper for [addMonitor(android.app.Instrumentation.ActivityMonitor)](../android/app/Instrumentation.md))that creates a class matching [ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md) for you and returns it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addResults](../android/app/Instrumentation.md))`(`results:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Report some results in the middle of instrumentation execution. Later results (including those provided by [finish](../android/app/Instrumentation.md))) will be combined with android.os.Bundle#putAll. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnCreate](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`, `icicle:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Perform calling of an activity's android.app.Activity#onCreate method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnCreate](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`, `icicle:` ` [Bundle](../android/os/Bundle.md)!`, `persistentState:` ` [PersistableBundle](../android/os/PersistableBundle.md)!`)` <br /> Perform calling of an activity's android.app.Activity#onCreate method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnDestroy](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnNewIntent](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`, `intent:` ` [Intent](../android/content/Intent.md)!`)` <br /> Perform calling of an activity's android.app.Activity#onNewIntent method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnNewIntent](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `intent:` ` [Intent](../android/content/Intent.md)`, `caller:` ` [ComponentCaller](../android/app/ComponentCaller.md)`)` <br /> Same as [callActivityOnNewIntent(android.app.Activity,android.content.Intent)](../android/app/Instrumentation.md)), but with an extra parameter for the [ComponentCaller](../android/app/ComponentCaller.md) instance associated with the app that sent the intent. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnPause](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`)` <br /> Perform calling of an activity's [Activity.onPause](../android/app/Activity.md))method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnPictureInPictureRequested](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)`)` <br /> Perform calling of an activity's [Activity.onPictureInPictureRequested](../android/app/Activity.md))method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnPostCreate](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)?`)` <br /> Perform calling of an activity's android.app.Activity#onPostCreate method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnPostCreate](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)?`, `persistentState:` ` [PersistableBundle](../android/os/PersistableBundle.md)?`)` <br /> Perform calling of an activity's android.app.Activity#onPostCreate method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnRestart](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`)` <br /> Perform calling of an activity's [Activity.onRestart](../android/app/Activity.md))method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnRestoreInstanceState](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)`)` <br /> Perform calling of an activity's android.app.Activity#onRestoreInstanceState method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnRestoreInstanceState](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `savedInstanceState:` ` [Bundle](../android/os/Bundle.md)?`, `persistentState:` ` [PersistableBundle](../android/os/PersistableBundle.md)?`)` <br /> Perform calling of an activity's android.app.Activity#onRestoreInstanceState method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnResume](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`)` <br /> Perform calling of an activity's [Activity.onResume](../android/app/Activity.md))method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnSaveInstanceState](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `outState:` ` [Bundle](../android/os/Bundle.md)`)` <br /> Perform calling of an activity's android.app.Activity#onSaveInstanceState method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnSaveInstanceState](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)`, `outState:` ` [Bundle](../android/os/Bundle.md)`, `outPersistentState:` ` [PersistableBundle](../android/os/PersistableBundle.md)`)` <br /> Perform calling of an activity's android.app.Activity#onSaveInstanceState method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnStart](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`)` <br /> Perform calling of an activity's [Activity.onStart](../android/app/Activity.md))method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnStop](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`)` <br /> Perform calling of an activity's [Activity.onStop](../android/app/Activity.md))method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callActivityOnUserLeaving](../android/app/Instrumentation.md))`(`activity:` ` [Activity](../android/app/Activity.md)!`)` <br /> Perform calling of an activity's [Activity.onUserLeaveHint](../android/app/Activity.md))method. The default implementation simply calls through to that method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [callApplicationOnCreate](../android/app/Instrumentation.md))`(`app:` ` [Application](../android/app/Application.md)!`)` <br /> Perform calling of the application's [Application.onCreate](../android/app/Application.md))method. The default implementation simply calls through to that method. Note: This method will be called immediately after [onCreate(android.os.Bundle)](../android/app/Instrumentation.md)). Often instrumentation tests start their test thread in onCreate(); you need to be careful of races between these. (Well between it and everything else, but let's start here.) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [checkMonitorHit](../android/app/Instrumentation.md))`(`monitor:` ` [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!`, `minHits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Test whether an existing [ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md) has been hit. If the monitor has been hit at least minHits times, then it will be removed from the activity monitor list and true returned. Otherwise it is left as-is and false is returned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endPerformanceSnapshot](../android/app/Instrumentation.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finish](../android/app/Instrumentation.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `results:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Terminate instrumentation of the application. This will cause the application process to exit, removing this instrumentation from the next time the application is started. If multiple processes are currently running for this instrumentation, all of those processes will be killed. <br /> | | [Bundle](../android/os/Bundle.md)! | [getAllocCounts](../android/app/Instrumentation.md))`()` <br /> Returns a bundle with the current results from the allocation counting. <br /> | | [Bundle](../android/os/Bundle.md)! | [getBinderCounts](../android/app/Instrumentation.md))`()` <br /> Returns a bundle with the counts for various binder counts for this process. Currently the only two that are reported are the number of send and the number of received transactions. <br /> | | [ComponentName](../android/content/ComponentName.md)! | [getComponentName](../android/app/Instrumentation.md))`()` <br /> Returns complete component name of this instrumentation. <br /> | | [Context](../android/content/Context.md)! | [getContext](../android/app/Instrumentation.md))`()` <br /> Return the Context of this instrumentation's package. Note that this is often different than the Context of the application being instrumentated, since the instrumentation code often lives is a different package than that of the application it is running against. See [getTargetContext](../android/app/Instrumentation.md))to retrieve a Context for the target application. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getProcessName](../android/app/Instrumentation.md))`()` <br /> Return the name of the process this instrumentation is running in. Note this should only be used for testing and debugging. If you are thinking about using this to, for example, conditionalize what is initialized in an Application class, it is strongly recommended to instead use lazy initialization (such as a getter for the state that only creates it when requested). This can greatly reduce the work your process does when created for secondary things, such as to receive a broadcast. <br /> | | [Context](../android/content/Context.md)! | [getTargetContext](../android/app/Instrumentation.md))`()` <br /> Return a Context for the target application being instrumented. Note that this is often different than the Context of the instrumentation code, since the instrumentation code often lives is a different package than that of the application it is running against. See [getContext](../android/app/Instrumentation.md))to retrieve a Context for the instrumentation code. <br /> | | [UiAutomation](../android/app/UiAutomation.md)! | [getUiAutomation](../android/app/Instrumentation.md))`()` <br /> Gets the [UiAutomation](../android/app/UiAutomation.md) instance with no flags set. **Note:** The APIs exposed via the returned [UiAutomation](../android/app/UiAutomation.md) work across application boundaries while the APIs exposed by the instrumentation do not. For example, [Instrumentation.sendPointerSync(MotionEvent)](../android/app/Instrumentation.md))will not allow you to inject the event in an app different from the instrumentation target, while [UiAutomation.injectInputEvent(android.view.InputEvent, boolean)](../android/app/UiAutomation.md))will work regardless of the current application. A typical test case should be using either the [UiAutomation](../android/app/UiAutomation.md) or [Instrumentation](../android/app/Instrumentation.md) APIs. Using both APIs at the same time is not a mistake by itself but a client has to be aware of the APIs limitations. Equivalent to`getUiAutomation(0)`. If a [UiAutomation](../android/app/UiAutomation.md) exists with different flags, the flags on that instance will be changed, and then it will be returned. Compatibility mode: This method is infallible for apps targeted for [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) and earlier versions; for apps targeted for later versions, it will return null if [UiAutomation](../android/app/UiAutomation.md) fails to connect. The caller can check the return value and retry on error. <br /> | | [UiAutomation](../android/app/UiAutomation.md)! | [getUiAutomation](../android/app/Instrumentation.md))`(`flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the [UiAutomation](../android/app/UiAutomation.md) instance with flags set. **Note:** The APIs exposed via the returned [UiAutomation](../android/app/UiAutomation.md) work across application boundaries while the APIs exposed by the instrumentation do not. For example, [Instrumentation.sendPointerSync(MotionEvent)](../android/app/Instrumentation.md))will not allow you to inject the event in an app different from the instrumentation target, while [UiAutomation.injectInputEvent(android.view.InputEvent, boolean)](../android/app/UiAutomation.md))will work regardless of the current application. A typical test case should be using either the [UiAutomation](../android/app/UiAutomation.md) or [Instrumentation](../android/app/Instrumentation.md) APIs. Using both APIs at the same time is not a mistake by itself but a client has to be aware of the APIs limitations. If a [UiAutomation](../android/app/UiAutomation.md) exists with different flags, the flags on that instance will be changed, and then it will be returned. Compatibility mode: This method is infallible for apps targeted for [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) and earlier versions; for apps targeted for later versions, it will return null if [UiAutomation](../android/app/UiAutomation.md) fails to connect. The caller can check the return value and retry on error. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [invokeContextMenuAction](../android/app/Instrumentation.md))`(`targetActivity:` ` [Activity](../android/app/Activity.md)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Show the context menu for the currently focused view and executes a particular context menu item. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [invokeMenuActionSync](../android/app/Instrumentation.md))`(`targetActivity:` ` [Activity](../android/app/Activity.md)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Execute a particular menu item. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isProfiling](../android/app/Instrumentation.md))`()` <br /> Check whether this instrumentation was started with profiling enabled. <br /> | | [Activity](../android/app/Activity.md)! | [newActivity](../android/app/Instrumentation.md))`(`clazz:` ` [Class](../java/lang/Class.md)<*>!`, `context:` ` [Context](../android/content/Context.md)!`, `token:` ` [IBinder](../android/os/IBinder.md)!`, `application:` ` [Application](../android/app/Application.md)!`, `intent:` ` [Intent](../android/content/Intent.md)!`, `info:` ` [ActivityInfo](../android/content/pm/ActivityInfo.md)!`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `parent:` ` [Activity](../android/app/Activity.md)!`, `id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `lastNonConfigurationInstance:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Perform instantiation of an [Activity](../android/app/Activity.md) object. This method is intended for use with unit tests, such as android.test.ActivityUnitTestCase. The activity will be useable locally but will be missing some of the linkages necessary for use within the system. <br /> | | [Activity](../android/app/Activity.md)! | [newActivity](../android/app/Instrumentation.md))`(`cl:` ` [ClassLoader](../java/lang/ClassLoader.md)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `intent:` ` [Intent](../android/content/Intent.md)!`)` <br /> Perform instantiation of the process's [Activity](../android/app/Activity.md) object. The default implementation provides the normal system behavior. <br /> | | [Application](../android/app/Application.md)! | [newApplication](../android/app/Instrumentation.md))`(`cl:` ` [ClassLoader](../java/lang/ClassLoader.md)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `context:` ` [Context](../android/content/Context.md)!`)` <br /> Perform instantiation of the process's [Application](../android/app/Application.md) object. The default implementation provides the normal system behavior. <br /> | | [Application](../android/app/Application.md)! | [newApplication](../android/app/Instrumentation.md))`(`clazz:` ` [Class](../java/lang/Class.md)<*>!`, `context:` ` [Context](../android/content/Context.md)!`)` <br /> Perform instantiation of the process's [Application](../android/app/Application.md) object. The default implementation provides the normal system behavior. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDestroy](../android/app/Instrumentation.md))`()` <br /> Called when the instrumented application is stopping, after all of the normal application cleanup has occurred. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onException](../android/app/Instrumentation.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `e:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> This is called whenever the system captures an unhandled exception that was thrown by the application. The default implementation simply returns false, allowing normal system handling of the exception to take place. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeMonitor](../android/app/Instrumentation.md))`(`monitor:` ` [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!`)` <br /> Remove an [ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md) that was previously added with #addMonitor. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetInTouchMode](../android/app/Instrumentation.md))`()` <br /> Resets the [touch mode](../android/app/Instrumentation.md))to the device default. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runOnMainSync](../android/app/Instrumentation.md))`(`runner:` ` [Runnable](../java/lang/Runnable.md)!`)` <br /> Execute a call on the application's main thread, blocking until it is complete. Useful for doing things that are not thread-safe, such as looking at or modifying the view hierarchy. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendCharacterSync](../android/app/Instrumentation.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends up and down key events with the given key code to the currently focused window, and waits for it to be processed. Equivalent to [sendKeyDownUpSync(int)](../android/app/Instrumentation.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeyDownUpSync](../android/app/Instrumentation.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends up and down key events with the given key code to the currently focused window, and waits for it to be processed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeySync](../android/app/Instrumentation.md))`(`event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Sends a key event to the currently focused window, and waits for it to be processed. This method blocks until the recipient has finished handling the event. Note that the recipient may*not*have completely finished reacting from the event when this method returns. For example, it may still be in the process of updating its display or UI contents upon reacting to the injected event. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendPointerSync](../android/app/Instrumentation.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` <br /> Dispatches a pointer event into a window owned by the instrumented application, and waits for it to be processed. If the motion event being injected is targeted at a window that is not owned by the instrumented application, the input injection will fail. See [getUiAutomation()](../android/app/Instrumentation.md))for injecting events into all windows. This method blocks until the recipient has finished handling the event. Note that the recipient may*not*have completely finished reacting from the event when this method returns. For example, it may still be in the process of updating its display or UI contents upon reacting to the injected event. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendStatus](../android/app/Instrumentation.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `results:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Provide a status report about the application. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendStringSync](../android/app/Instrumentation.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends the key events that result in the given text being typed into the currently focused window, and waits for it to be processed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendTrackballEventSync](../android/app/Instrumentation.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` <br /> Dispatches a trackball event into the currently focused window, and waits for it to be processed. This method blocks until the recipient has finished handling the event. Note that the recipient may*not*have completely finished reacting from the event when this method returns. For example, it may still be in the process of updating its display or UI contents upon reacting to the injected event. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutomaticPerformanceSnapshots](../android/app/Instrumentation.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInTouchMode](../android/app/Instrumentation.md))`(`inTouch:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Force the global system in or out of touch mode. This can be used if your instrumentation relies on the UI being in one more or the other when it starts. **Note:** Starting from Android [Build.VERSION_CODES.TIRAMISU](../android/os/Build.VERSION_CODES.md), this method will only take effect if the instrumentation was sourced from a process with`MODIFY_TOUCH_MODE_STATE`internal permission granted (shell already have it). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/app/Instrumentation.md))`()` <br /> Create and start a new thread in which to run instrumentation. This new thread will call to [onStart](../android/app/Instrumentation.md))where you can implement the instrumentation. <br /> | | [Activity](../android/app/Activity.md)! | [startActivitySync](../android/app/Instrumentation.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`)` <br /> Start a new activity and wait for it to begin running before returning. In addition to being synchronous, this method as some semantic differences from the standard android.content.Context#startActivity call: the activity component is resolved before talking with the activity manager (its class name is specified in the Intent that this method ultimately starts), and it does not allow you to start activities that run in a different process. In addition, if the given Intent resolves to multiple activities, instead of displaying a dialog for the user to select an activity, an exception will be thrown. The function returns as soon as the activity goes idle following the call to its android.app.Activity#onCreate. Generally this means it has gone through the full initialization including [Activity.onResume](../android/app/Activity.md))and drawn and displayed its initial window. <br /> | | [Activity](../android/app/Activity.md) | [startActivitySync](../android/app/Instrumentation.md))`(`intent:` ` [Intent](../android/content/Intent.md)`, `options:` ` [Bundle](../android/os/Bundle.md)?`)` <br /> Start a new activity and wait for it to begin running before returning. In addition to being synchronous, this method as some semantic differences from the standard android.content.Context#startActivity call: the activity component is resolved before talking with the activity manager (its class name is specified in the Intent that this method ultimately starts), and it does not allow you to start activities that run in a different process. In addition, if the given Intent resolves to multiple activities, instead of displaying a dialog for the user to select an activity, an exception will be thrown. The function returns as soon as the activity goes idle following the call to its android.app.Activity#onCreate. Generally this means it has gone through the full initialization including [Activity.onResume](../android/app/Activity.md))and drawn and displayed its initial window. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAllocCounting](../android/app/Instrumentation.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startPerformanceSnapshot](../android/app/Instrumentation.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startProfiling](../android/app/Instrumentation.md))`()` <br /> This method will start profiling if isProfiling() returns true. You should only call this method if you set the handleProfiling attribute in the manifest file for this Instrumentation to true. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopAllocCounting](../android/app/Instrumentation.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopProfiling](../android/app/Instrumentation.md))`()` <br /> Stops profiling if isProfiling() returns true. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [waitForIdle](../android/app/Instrumentation.md))`(`recipient:` ` [Runnable](../java/lang/Runnable.md)!`)` <br /> Schedule a callback for when the application's main thread goes idle (has no more events to process). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [waitForIdleSync](../android/app/Instrumentation.md))`()` <br /> Synchronously wait for the application to be idle. Can not be called from the main application thread -- use [start](../android/app/Instrumentation.md))to execute instrumentation in its own thread. <br /> | | [Activity](../android/app/Activity.md)! | [waitForMonitor](../android/app/Instrumentation.md))`(`monitor:` ` [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!`)` <br /> Wait for an existing [ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md) to be hit. Once the monitor has been hit, it is removed from the activity monitor list and the first created Activity object that matched it is returned. <br /> | | [Activity](../android/app/Activity.md)! | [waitForMonitorWithTimeout](../android/app/Instrumentation.md))`(`monitor:` ` [Instrumentation.ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md)!`, `timeOut:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Wait for an existing [ActivityMonitor](../android/app/Instrumentation.ActivityMonitor.md) to be hit till the timeout expires. Once the monitor has been hit, it is removed from the activity monitor list and the first created Activity object that matched it is returned. If the timeout expires, a null object is returned. <br /> | ||

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

This value, if stored with key [android.app.Instrumentation#REPORT_KEY_IDENTIFIER](../android/app/Instrumentation.md), identifies InstrumentationTestRunner as the source of the report. This is sent with all status messages. 

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
| [Bundle](../android/os/Bundle.md)! | the Bundle object |

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
| `arguments` | [Bundle](../android/os/Bundle.md)!:Any additional arguments that were supplied when the instrumentation was started. |

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
