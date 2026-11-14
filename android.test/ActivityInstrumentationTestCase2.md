# ActivityInstrumentationTestCase2

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityInstrumentationTestCase2

Kotlin| [Java](https://developer.android.com/reference/android/test/ActivityInstrumentationTestCase2 "View this page in Java") 
| --- | --- |

```
abstract class ActivityInstrumentationTestCase2<T : Activity!> : ActivityTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) |||
| | ↳ | [android.test.ActivityTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase) ||
| | | ↳ | [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 24.**
|
| Use [ActivityTestRule](https://developer.android.com/reference/android/support/test/rule/ActivityTestRule.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This class provides functional testing of a single activity. The activity under test will be created using the system infrastructure (by calling InstrumentationTestCase.launchActivity()) and you will then be able to manipulate your Activity directly.

Other options supported by this test case include:

- You can run any test method on the UI thread (see [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest)).
- You can inject custom Intents into your Activity (see [setActivityIntent(android.content.Intent)](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setActivityIntent(android.content.Intent))).

This class replaces [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase), which is deprecated. New tests should be written using this base class.

If you prefer an isolated unit test, see [android.test.ActivityUnitTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#ActivityInstrumentationTestCase2(java.lang.Class))`(`activityClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` Creates an [ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#). |
| [ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#ActivityInstrumentationTestCase2(kotlin.String,%20java.lang.Class))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` Creates an [ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#). |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT | [getActivity](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#getActivity())`()` Get the Activity under test, starting it if necessary. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivityInitialTouchMode](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setActivityInitialTouchMode(kotlin.Boolean))`(`initialTouchMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Call this method before the first call to [getActivity](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#getActivity())to set the initial touch mode for the Activity under test. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivityIntent](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setActivityIntent(android.content.Intent))`(`i:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Call this method before the first call to [getActivity](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#getActivity())to inject a customized Intent into the Activity under test. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#runTest())`()` Runs the current unit test. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setUp())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#tearDown())`()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)! | [getInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#getInstrumentation())`()` <br /> Inheritors can access the instrumentation using this. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInsrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInsrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInstrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | T | [launchActivity](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivity(kotlin.String,%20java.lang.Class,%20android.os.Bundle))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Utility method for launching an activity. The [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) used to launch the Activity is: action = [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) extras = null, unless a custom bundle is provided here All other fields are null or empty. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | T | [launchActivityWithIntent](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivityWithIntent(kotlin.String,%20java.lang.Class,%20android.content.Intent))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` <br /> Utility method for launching an activity with a specific Intent. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTest())`()` <br /> Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), the test is run on the UI thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTestOnUiThread](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTestOnUiThread(java.lang.Runnable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Helper for running portions of a test on the UI thread. Note, in most cases it is simpler to annotate the test method with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), which will run the entire test method on the UI thread. Use this method if you need to switch in and out of the UI thread to perform your test. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. For instance: sendKeys(KEYCODE_DPAD_LEFT, KEYCODE_DPAD_CENTER). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.String))`(`keysSequence:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends a series of key events through instrumentation and waits for idle. The sequence of keys is a string containing the key names as specified in KeyEvent, without the KEYCODE_ prefix. For instance: sendKeys("DPAD_LEFT A B C DPAD_CENTER"). Each key can be repeated by using the N\* prefix. For instance, to send two KEYCODE_DPAD_LEFT, use the following: sendKeys("2\*DPAD_LEFT"). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRepeatedKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendRepeatedKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. Each key code must be preceded by the number of times the key code must be sent. For instance: sendRepeatedKeys(1, KEYCODE_DPAD_CENTER, 2, KEYCODE_DPAD_LEFT). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#tearDown())`()` <br /> Make sure all resources are cleaned up and garbage collected before moving on to the next test. Subclasses that override this method should make sure they call super.tearDown() at the end of the overriding method. <br /> | ||
| From class [ActivityTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase#scrubClass(java.lang.Class))`(`testCaseClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` <br /> This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivity](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase#setActivity(android.app.Activity))`(`testActivity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` <br /> Set the activity under test. <br /> | ||

## Public constructors

### ActivityInstrumentationTestCase2

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ActivityInstrumentationTestCase2(activityClass: Class<T>!)
```

Creates an [ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#).

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activityClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:The activity to test. This must be a class in the instrumentation targetPackage specified in the AndroidManifest.xml |

### ActivityInstrumentationTestCase2

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ActivityInstrumentationTestCase2(
    pkg: String!, 
    activityClass: Class<T>!)
```

**Deprecated:** *use [ActivityInstrumentationTestCase2(java.lang.Class)](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#ActivityInstrumentationTestCase2(java.lang.Class))instead*

Creates an [ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#).

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:ignored - no longer in use. |
| `activityClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:The activity to test. This must be a class in the instrumentation targetPackage specified in the AndroidManifest.xml |

## Public methods

### getActivity

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActivity(): T
```

**Deprecated:** *Deprecated in Java.*

Get the Activity under test, starting it if necessary. For each test method invocation, the Activity will not actually be created until the first time this method is called.

If you wish to provide custom setup values to your Activity, you may call [setActivityIntent(android.content.Intent)](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setActivityIntent(android.content.Intent))and/or [setActivityInitialTouchMode(boolean)](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setActivityInitialTouchMode(kotlin.Boolean))before your first call to getActivity(). Calling them after your Activity has started will have no effect.

**NOTE:** Activities under test may not be started from within the UI thread. If your test method is annotated with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), then your Activity will be started automatically just before your test method is run. You still call this method in order to get the Activity under test.

| Return ||
|---|-------------------------|
| T | the Activity under test |

### setActivityInitialTouchMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setActivityInitialTouchMode(initialTouchMode: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Call this method before the first call to [getActivity](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#getActivity())to set the initial touch mode for the Activity under test.

If you do not call this, the touch mode will be false. If you call this after your Activity has been started, it will have no effect.

**NOTE:** Activities under test may not be started from within the UI thread. If your test method is annotated with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), then you must call [setActivityInitialTouchMode(boolean)](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setActivityInitialTouchMode(kotlin.Boolean))from [setUp()](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setUp()).

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialTouchMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the Activity should be placed into "touch mode" when started |

### setActivityIntent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setActivityIntent(i: Intent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Call this method before the first call to [getActivity](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#getActivity())to inject a customized Intent into the Activity under test.

If you do not call this, the default intent will be provided. If you call this after your Activity has been started, it will have no effect.

**NOTE:** Activities under test may not be started from within the UI thread. If your test method is annotated with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), then you must call [setActivityIntent(android.content.Intent)](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setActivityIntent(android.content.Intent))from [setUp()](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2#setUp()).

The default Intent (if this method is not called) is: action = [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) flags = [Intent.FLAG_ACTIVITY_NEW_TASK](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK:kotlin.Int) All other fields are null or empty.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The Intent to start the Activity with, or null to reset to the default Intent. |

## Protected methods

### runTest

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun runTest(): Unit
```

**Deprecated:** *Deprecated in Java.*

Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), force the Activity to be created before switching to the UI thread. 

### setUp

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setUp(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### tearDown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun tearDown(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |
