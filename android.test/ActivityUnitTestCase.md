# ActivityUnitTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityUnitTestCase

Kotlin| [Java](https://developer.android.com/reference/android/test/ActivityUnitTestCase "View this page in Java") 
| --- | --- |

```
abstract class ActivityUnitTestCase<T : Activity!> : ActivityTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) |||
| | ↳ | [android.test.ActivityTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase) ||
| | | ↳ | [android.test.ActivityUnitTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 24.**
|
| Write [Local Unit Tests](https://developer.android.com/training/testing/unit-testing/local-unit-tests.html) instead.

This class provides isolated testing of a single activity. The activity under test will be created with minimal connection to the system infrastructure, and you can inject mocked or wrappered versions of many of Activity's dependencies. Most of the work is handled automatically here by [setUp](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#setUp())and [tearDown](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#tearDown()).

If you prefer a functional test, see [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase).

It must be noted that, as a true unit test, your Activity will not be running in the normal system and will not participate in the normal interactions with other Activities. The following methods should not be called in this configuration - most of them will throw exceptions:

- [android.app.Activity#createPendingResult(int, Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#createPendingResult(kotlin.Int,%20android.content.Intent,%20kotlin.Int))
- [android.app.Activity#startActivityIfNeeded(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityIfNeeded(android.content.Intent,%20kotlin.Int))
- [android.app.Activity#startActivityFromChild(Activity, Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityFromChild(android.app.Activity,%20android.content.Intent,%20kotlin.Int))
- [android.app.Activity#startNextMatchingActivity(Intent)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startNextMatchingActivity(android.content.Intent))
- [android.app.Activity#getCallingActivity()](https://developer.android.com/reference/kotlin/android/app/Activity.html#getCallingActivity())
- [android.app.Activity#getCallingPackage()](https://developer.android.com/reference/kotlin/android/app/Activity.html#getCallingPackage())
- [android.app.Activity#createPendingResult(int, Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#createPendingResult(kotlin.Int,%20android.content.Intent,%20kotlin.Int))
- [android.app.Activity#getTaskId()](https://developer.android.com/reference/kotlin/android/app/Activity.html#getTaskId())
- [android.app.Activity#isTaskRoot()](https://developer.android.com/reference/kotlin/android/app/Activity.html#isTaskRoot())
- [android.app.Activity#moveTaskToBack(boolean)](https://developer.android.com/reference/kotlin/android/app/Activity.html#moveTaskToBack(kotlin.Boolean))

The following methods may be called but will not do anything. For test purposes, you can use the methods [getStartedActivityIntent()](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#getStartedActivityIntent())and [getStartedActivityRequest()](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#getStartedActivityRequest())to inspect the parameters that they were called with.

- android.app.Activity#startActivity(Intent)
- [android.app.Activity#startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int))

The following methods may be called but will not do anything. For test purposes, you can use the methods [isFinishCalled()](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#isFinishCalled())and [getFinishedActivityRequest()](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#getFinishedActivityRequest())to inspect the parameters that they were called with.

- [android.app.Activity#finish()](https://developer.android.com/reference/kotlin/android/app/Activity.html#finish())
- [android.app.Activity#finishFromChild(Activity child)](https://developer.android.com/reference/kotlin/android/app/Activity.html#finishFromChild(android.app.Activity))
- [android.app.Activity#finishActivity(int requestCode)](https://developer.android.com/reference/kotlin/android/app/Activity.html#finishActivity(kotlin.Int))

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ActivityUnitTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#ActivityUnitTestCase(java.lang.Class))`(`activityClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT | [getActivity](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#getActivity())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFinishedActivityRequest](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#getFinishedActivityRequest())`()` This method will return the request code if the Activity under test called [android.app.Activity#finishActivity(int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#finishActivity(kotlin.Int)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestedOrientation](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#getRequestedOrientation())`()` This method will return the value if your Activity under test calls [android.app.Activity#setRequestedOrientation](https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)). |
| --- | --- |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | [getStartedActivityIntent](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#getStartedActivityIntent())`()` This method will return the launch intent if your Activity under test calls android. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStartedActivityRequest](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#getStartedActivityRequest())`()` This method will return the launch request code if your Activity under test calls [android.app.Activity#startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinishCalled](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#isFinishCalled())`()` This method will notify you if the Activity under test called [android.app.Activity#finish()](https://developer.android.com/reference/kotlin/android/app/Activity.html#finish()), [android.app.Activity#finishFromChild(Activity)](https://developer.android.com/reference/kotlin/android/app/Activity.html#finishFromChild(android.app.Activity)), or [android.app.Activity#finishActivity(int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#finishActivity(kotlin.Int)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivityContext](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#setActivityContext(android.content.Context))`(`activityContext:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` If you wish to inject a Mock, Isolated, or otherwise altered context, you can do so here. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setApplication](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#setApplication(android.app.Application))`(`application:` ` [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)!`)` Set the application for use during the test. |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#setUp())`()` <br /> |
| openT | [startActivity](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#startActivity(android.content.Intent,%20android.os.Bundle,%20kotlin.Any))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `savedInstanceState:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `lastNonConfigurationInstance:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Start the activity under test, in the same way as if it was started by android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#tearDown())`()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)! | [getInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#getInstrumentation())`()` <br /> Inheritors can access the instrumentation using this. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInsrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInsrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInstrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | T | [launchActivity](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivity(kotlin.String,%20java.lang.Class,%20android.os.Bundle))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Utility method for launching an activity. The [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) used to launch the Activity is: action = [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) extras = null, unless a custom bundle is provided here All other fields are null or empty. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | T | [launchActivityWithIntent](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivityWithIntent(kotlin.String,%20java.lang.Class,%20android.content.Intent))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` <br /> Utility method for launching an activity with a specific Intent. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTest())`()` <br /> Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), the test is run on the UI thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTestOnUiThread](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTestOnUiThread(java.lang.Runnable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Helper for running portions of a test on the UI thread. Note, in most cases it is simpler to annotate the test method with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), which will run the entire test method on the UI thread. Use this method if you need to switch in and out of the UI thread to perform your test. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. For instance: sendKeys(KEYCODE_DPAD_LEFT, KEYCODE_DPAD_CENTER). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.String))`(`keysSequence:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends a series of key events through instrumentation and waits for idle. The sequence of keys is a string containing the key names as specified in KeyEvent, without the KEYCODE_ prefix. For instance: sendKeys("DPAD_LEFT A B C DPAD_CENTER"). Each key can be repeated by using the N\* prefix. For instance, to send two KEYCODE_DPAD_LEFT, use the following: sendKeys("2\*DPAD_LEFT"). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRepeatedKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendRepeatedKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. Each key code must be preceded by the number of times the key code must be sent. For instance: sendRepeatedKeys(1, KEYCODE_DPAD_CENTER, 2, KEYCODE_DPAD_LEFT). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#tearDown())`()` <br /> Make sure all resources are cleaned up and garbage collected before moving on to the next test. Subclasses that override this method should make sure they call super.tearDown() at the end of the overriding method. <br /> | ||
| From class [ActivityTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase#scrubClass(java.lang.Class))`(`testCaseClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` <br /> This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivity](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase#setActivity(android.app.Activity))`(`testActivity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` <br /> Set the activity under test. <br /> | ||

## Public constructors

### ActivityUnitTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ActivityUnitTestCase(activityClass: Class<T>!)
```

## Public methods

### getActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActivity(): T
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|----------------------------------|
| T | Returns the activity under test. |

### getFinishedActivityRequest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFinishedActivityRequest(): Int
```

**Deprecated:** *Deprecated in Java.*

This method will return the request code if the Activity under test called [android.app.Activity#finishActivity(int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#finishActivity(kotlin.Int)).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The request code provided in the start call, or -1 if no finish call was made. |

### getRequestedOrientation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequestedOrientation(): Int
```

**Deprecated:** *Deprecated in Java.*

This method will return the value if your Activity under test calls [android.app.Activity#setRequestedOrientation](https://developer.android.com/reference/kotlin/android/app/Activity.html#setRequestedOrientation(kotlin.Int)). 

### getStartedActivityIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStartedActivityIntent(): Intent!
```

**Deprecated:** *Deprecated in Java.*

This method will return the launch intent if your Activity under test calls android.app.Activity#startActivity(Intent) or [android.app.Activity#startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)).

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | The Intent provided in the start call, or null if no start call was made. |

### getStartedActivityRequest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStartedActivityRequest(): Int
```

**Deprecated:** *Deprecated in Java.*

This method will return the launch request code if your Activity under test calls [android.app.Activity#startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The request code provided in the start call, or -1 if no start call was made. |

### isFinishCalled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFinishCalled(): Boolean
```

**Deprecated:** *Deprecated in Java.*

This method will notify you if the Activity under test called [android.app.Activity#finish()](https://developer.android.com/reference/kotlin/android/app/Activity.html#finish()), [android.app.Activity#finishFromChild(Activity)](https://developer.android.com/reference/kotlin/android/app/Activity.html#finishFromChild(android.app.Activity)), or [android.app.Activity#finishActivity(int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#finishActivity(kotlin.Int)).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns true if one of the listed finish methods was called. |

### setActivityContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setActivityContext(activityContext: Context!): Unit
```

**Deprecated:** *Deprecated in Java.*

If you wish to inject a Mock, Isolated, or otherwise altered context, you can do so here. You must call this function before calling [startActivity](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#startActivity(android.content.Intent,%20android.os.Bundle,%20kotlin.Any)). If you wish to obtain a real Context, as a building block, use getInstrumentation().getTargetContext(). 

### setApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setApplication(application: Application!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the application for use during the test. You must call this function before calling [startActivity](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#startActivity(android.content.Intent,%20android.os.Bundle,%20kotlin.Any)). If your test does not call this method,

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `application` | [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)!:The Application object that will be injected into the Activity under test. |

## Protected methods

### setUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setUp(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### startActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun startActivity(
    intent: Intent!, 
    savedInstanceState: Bundle!, 
    lastNonConfigurationInstance: Any!
): T
```

**Deprecated:** *Deprecated in Java.*

Start the activity under test, in the same way as if it was started by android.content.Context#startActivity, providing the arguments it supplied. When you use this method to start the activity, it will automatically be stopped by [tearDown](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase#tearDown()).

This method will call onCreate(), but if you wish to further exercise Activity life cycle methods, you must call them yourself from your test case.

*Do not call from your setUp() method. You must call this method from each of your test methods.*

| Parameters ||
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The Intent as if supplied to android.content.Context#startActivity. |
| `savedInstanceState` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:The instance state, if you are simulating this part of the life cycle. Typically null. |
| `lastNonConfigurationInstance` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:This Object will be available to the Activity if it calls [android.app.Activity#getLastNonConfigurationInstance()](https://developer.android.com/reference/kotlin/android/app/Activity.html#getLastNonConfigurationInstance()). Typically null. |
| --- | --- |

| Return ||
|---|---------------------------------------|
| T | Returns the Activity that was created |

### tearDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun tearDown(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |
