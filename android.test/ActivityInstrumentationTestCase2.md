# ActivityInstrumentationTestCase2

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityInstrumentationTestCase2

Kotlin| [Java](../android/test/ActivityInstrumentationTestCase2.md) 
| --- | --- |

```
abstract class ActivityInstrumentationTestCase2<T : Activity!> : ActivityTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md) |||
| | ↳ | [android.test.ActivityTestCase](../android/test/ActivityTestCase.md) ||
| | | ↳ | [android.test.ActivityInstrumentationTestCase2](../android/test/ActivityInstrumentationTestCase2.md) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 24.**
|
| Use [ActivityTestRule](../android/support/test/rule/ActivityTestRule.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This class provides functional testing of a single activity. The activity under test will be created using the system infrastructure (by calling InstrumentationTestCase.launchActivity()) and you will then be able to manipulate your Activity directly.

Other options supported by this test case include:

- You can run any test method on the UI thread (see [android.test.UiThreadTest](../android/test/UiThreadTest.md)).
- You can inject custom Intents into your Activity (see [setActivityIntent(android.content.Intent)](../android/test/ActivityInstrumentationTestCase2.md))).

This class replaces [android.test.ActivityInstrumentationTestCase](../android/test/ActivityInstrumentationTestCase.md), which is deprecated. New tests should be written using this base class.

If you prefer an isolated unit test, see [android.test.ActivityUnitTestCase](../android/test/ActivityUnitTestCase.md).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ActivityInstrumentationTestCase2](../android/test/ActivityInstrumentationTestCase2.md))`(`activityClass:` ` [Class](../java/lang/Class.md)<T>!`)` Creates an [ActivityInstrumentationTestCase2](../android/test/ActivityInstrumentationTestCase2.md). |
| [ActivityInstrumentationTestCase2](../android/test/ActivityInstrumentationTestCase2.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityClass:` ` [Class](../java/lang/Class.md)<T>!`)` Creates an [ActivityInstrumentationTestCase2](../android/test/ActivityInstrumentationTestCase2.md). |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT | [getActivity](../android/test/ActivityInstrumentationTestCase2.md))`()` Get the Activity under test, starting it if necessary. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivityInitialTouchMode](../android/test/ActivityInstrumentationTestCase2.md))`(`initialTouchMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Call this method before the first call to [getActivity](../android/test/ActivityInstrumentationTestCase2.md))to set the initial touch mode for the Activity under test. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivityIntent](../android/test/ActivityInstrumentationTestCase2.md))`(`i:` ` [Intent](../android/content/Intent.md)!`)` Call this method before the first call to [getActivity](../android/test/ActivityInstrumentationTestCase2.md))to inject a customized Intent into the Activity under test. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](../android/test/ActivityInstrumentationTestCase2.md))`()` Runs the current unit test. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](../android/test/ActivityInstrumentationTestCase2.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](../android/test/ActivityInstrumentationTestCase2.md))`()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [InstrumentationTestCase](../android/test/InstrumentationTestCase.md) |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Instrumentation](../android/app/Instrumentation.md)! | [getInstrumentation](../android/test/InstrumentationTestCase.md))`()` <br /> Inheritors can access the instrumentation using this. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInsrumentation](../android/test/InstrumentationTestCase.md))`(`instrumentation:` ` [Instrumentation](../android/app/Instrumentation.md)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInstrumentation](../android/test/InstrumentationTestCase.md))`(`instrumentation:` ` [Instrumentation](../android/app/Instrumentation.md)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | T | [launchActivity](../android/test/InstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](../java/lang/Class.md)<T>!`, `extras:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Utility method for launching an activity. The [Intent](../android/content/Intent.md) used to launch the Activity is: action = [Intent.ACTION_MAIN](../android/content/Intent.md) extras = null, unless a custom bundle is provided here All other fields are null or empty. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | T | [launchActivityWithIntent](../android/test/InstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](../java/lang/Class.md)<T>!`, `intent:` ` [Intent](../android/content/Intent.md)!`)` <br /> Utility method for launching an activity with a specific Intent. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](../android/test/InstrumentationTestCase.md))`()` <br /> Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](../android/test/UiThreadTest.md), the test is run on the UI thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTestOnUiThread](../android/test/InstrumentationTestCase.md))`(`r:` ` [Runnable](../java/lang/Runnable.md)!`)` <br /> Helper for running portions of a test on the UI thread. Note, in most cases it is simpler to annotate the test method with [android.test.UiThreadTest](../android/test/UiThreadTest.md), which will run the entire test method on the UI thread. Use this method if you need to switch in and out of the UI thread to perform your test. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](../android/test/InstrumentationTestCase.md))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. For instance: sendKeys(KEYCODE_DPAD_LEFT, KEYCODE_DPAD_CENTER). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](../android/test/InstrumentationTestCase.md))`(`keysSequence:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends a series of key events through instrumentation and waits for idle. The sequence of keys is a string containing the key names as specified in KeyEvent, without the KEYCODE_ prefix. For instance: sendKeys("DPAD_LEFT A B C DPAD_CENTER"). Each key can be repeated by using the N\* prefix. For instance, to send two KEYCODE_DPAD_LEFT, use the following: sendKeys("2\*DPAD_LEFT"). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRepeatedKeys](../android/test/InstrumentationTestCase.md))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. Each key code must be preceded by the number of times the key code must be sent. For instance: sendRepeatedKeys(1, KEYCODE_DPAD_CENTER, 2, KEYCODE_DPAD_LEFT). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](../android/test/InstrumentationTestCase.md))`()` <br /> Make sure all resources are cleaned up and garbage collected before moving on to the next test. Subclasses that override this method should make sure they call super.tearDown() at the end of the overriding method. <br /> | ||
| From class [ActivityTestCase](../android/test/ActivityTestCase.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](../android/test/ActivityTestCase.md))`(`testCaseClass:` ` [Class](../java/lang/Class.md)<*>!`)` <br /> This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivity](../android/test/ActivityTestCase.md))`(`testActivity:` ` [Activity](../android/app/Activity.md)!`)` <br /> Set the activity under test. <br /> | ||

## Public constructors

### ActivityInstrumentationTestCase2

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ActivityInstrumentationTestCase2(activityClass: Class<T>!)
```

Creates an [ActivityInstrumentationTestCase2](../android/test/ActivityInstrumentationTestCase2.md).

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activityClass` | [Class](../java/lang/Class.md)\<T\>!:The activity to test. This must be a class in the instrumentation targetPackage specified in the AndroidManifest.xml |

### ActivityInstrumentationTestCase2

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ActivityInstrumentationTestCase2(
    pkg: String!, 
    activityClass: Class<T>!)
```

**Deprecated:** *use [ActivityInstrumentationTestCase2(java.lang.Class)](../android/test/ActivityInstrumentationTestCase2.md))instead*

Creates an [ActivityInstrumentationTestCase2](../android/test/ActivityInstrumentationTestCase2.md).

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:ignored - no longer in use. |
| `activityClass` | [Class](../java/lang/Class.md)\<T\>!:The activity to test. This must be a class in the instrumentation targetPackage specified in the AndroidManifest.xml |

## Public methods

### getActivity

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActivity(): T
```

**Deprecated:** *Deprecated in Java.*

Get the Activity under test, starting it if necessary. For each test method invocation, the Activity will not actually be created until the first time this method is called.

If you wish to provide custom setup values to your Activity, you may call [setActivityIntent(android.content.Intent)](../android/test/ActivityInstrumentationTestCase2.md))and/or [setActivityInitialTouchMode(boolean)](../android/test/ActivityInstrumentationTestCase2.md))before your first call to getActivity(). Calling them after your Activity has started will have no effect.

**NOTE:** Activities under test may not be started from within the UI thread. If your test method is annotated with [android.test.UiThreadTest](../android/test/UiThreadTest.md), then your Activity will be started automatically just before your test method is run. You still call this method in order to get the Activity under test.

| Return ||
|---|-------------------------|
| T | the Activity under test |

### setActivityInitialTouchMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setActivityInitialTouchMode(initialTouchMode: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Call this method before the first call to [getActivity](../android/test/ActivityInstrumentationTestCase2.md))to set the initial touch mode for the Activity under test.

If you do not call this, the touch mode will be false. If you call this after your Activity has been started, it will have no effect.

**NOTE:** Activities under test may not be started from within the UI thread. If your test method is annotated with [android.test.UiThreadTest](../android/test/UiThreadTest.md), then you must call [setActivityInitialTouchMode(boolean)](../android/test/ActivityInstrumentationTestCase2.md))from [setUp()](../android/test/ActivityInstrumentationTestCase2.md)).

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialTouchMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the Activity should be placed into "touch mode" when started |

### setActivityIntent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setActivityIntent(i: Intent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Call this method before the first call to [getActivity](../android/test/ActivityInstrumentationTestCase2.md))to inject a customized Intent into the Activity under test.

If you do not call this, the default intent will be provided. If you call this after your Activity has been started, it will have no effect.

**NOTE:** Activities under test may not be started from within the UI thread. If your test method is annotated with [android.test.UiThreadTest](../android/test/UiThreadTest.md), then you must call [setActivityIntent(android.content.Intent)](../android/test/ActivityInstrumentationTestCase2.md))from [setUp()](../android/test/ActivityInstrumentationTestCase2.md)).

The default Intent (if this method is not called) is: action = [Intent.ACTION_MAIN](../android/content/Intent.md) flags = [Intent.FLAG_ACTIVITY_NEW_TASK](../android/content/Intent.md) All other fields are null or empty.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Intent](../android/content/Intent.md)!:The Intent to start the Activity with, or null to reset to the default Intent. |

## Protected methods

### runTest

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun runTest(): Unit
```

**Deprecated:** *Deprecated in Java.*

Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](../android/test/UiThreadTest.md), force the Activity to be created before switching to the UI thread. 

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
