# ActivityInstrumentationTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityInstrumentationTestCase

Kotlin| [Java](ActivityInstrumentationTestCase.md) 
| --- | --- |

```
abstract class ActivityInstrumentationTestCase<T : Activity!> : ActivityTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.test.InstrumentationTestCase](InstrumentationTestCase.md) |||
| | ↳ | [android.test.ActivityTestCase](ActivityTestCase.md) ||
| | | ↳ | [android.test.ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 3.**
|
| new tests should be written using [android.test.ActivityInstrumentationTestCase2](ActivityInstrumentationTestCase2.md), which provides more options for configuring the Activity under test

This class provides functional testing of a single activity. The activity under test will be created using the system infrastructure (by calling InstrumentationTestCase.launchActivity()) and you will then be able to manipulate your Activity directly. Most of the work is handled automatically here by [setUp](ActivityInstrumentationTestCase.md))and [tearDown](ActivityInstrumentationTestCase.md)).

If you prefer an isolated unit test, see [android.test.ActivityUnitTestCase](ActivityUnitTestCase.md).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityClass:` ` [Class](../java.lang/Class.md)<T>!`)` Creates an [ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md) in non-touch mode. |
| [ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityClass:` ` [Class](../java.lang/Class.md)<T>!`, `initialTouchMode:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates an [ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md). |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT | [getActivity](ActivityInstrumentationTestCase.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testActivityTestCaseSetUpProperly](ActivityInstrumentationTestCase.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](ActivityInstrumentationTestCase.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](ActivityInstrumentationTestCase.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [InstrumentationTestCase](InstrumentationTestCase.md) |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Instrumentation](../android.app/Instrumentation.md)! | [getInstrumentation](InstrumentationTestCase.md))`()` <br /> Inheritors can access the instrumentation using this. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInsrumentation](InstrumentationTestCase.md))`(`instrumentation:` ` [Instrumentation](../android.app/Instrumentation.md)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInstrumentation](InstrumentationTestCase.md))`(`instrumentation:` ` [Instrumentation](../android.app/Instrumentation.md)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | T | [launchActivity](InstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](../java.lang/Class.md)<T>!`, `extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> Utility method for launching an activity. The [Intent](../android.content/Intent.md) used to launch the Activity is: action = [Intent.ACTION_MAIN](../android.content/Intent.md) extras = null, unless a custom bundle is provided here All other fields are null or empty. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | T | [launchActivityWithIntent](InstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](../java.lang/Class.md)<T>!`, `intent:` ` [Intent](../android.content/Intent.md)!`)` <br /> Utility method for launching an activity with a specific Intent. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](InstrumentationTestCase.md))`()` <br /> Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](UiThreadTest.md), the test is run on the UI thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTestOnUiThread](InstrumentationTestCase.md))`(`r:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> Helper for running portions of a test on the UI thread. Note, in most cases it is simpler to annotate the test method with [android.test.UiThreadTest](UiThreadTest.md), which will run the entire test method on the UI thread. Use this method if you need to switch in and out of the UI thread to perform your test. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](InstrumentationTestCase.md))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. For instance: sendKeys(KEYCODE_DPAD_LEFT, KEYCODE_DPAD_CENTER). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](InstrumentationTestCase.md))`(`keysSequence:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends a series of key events through instrumentation and waits for idle. The sequence of keys is a string containing the key names as specified in KeyEvent, without the KEYCODE_ prefix. For instance: sendKeys("DPAD_LEFT A B C DPAD_CENTER"). Each key can be repeated by using the N\* prefix. For instance, to send two KEYCODE_DPAD_LEFT, use the following: sendKeys("2\*DPAD_LEFT"). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRepeatedKeys](InstrumentationTestCase.md))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. Each key code must be preceded by the number of times the key code must be sent. For instance: sendRepeatedKeys(1, KEYCODE_DPAD_CENTER, 2, KEYCODE_DPAD_LEFT). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](InstrumentationTestCase.md))`()` <br /> Make sure all resources are cleaned up and garbage collected before moving on to the next test. Subclasses that override this method should make sure they call super.tearDown() at the end of the overriding method. <br /> | ||
| From class [ActivityTestCase](ActivityTestCase.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](ActivityTestCase.md))`(`testCaseClass:` ` [Class](../java.lang/Class.md)<*>!`)` <br /> This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivity](ActivityTestCase.md))`(`testActivity:` ` [Activity](../android.app/Activity.md)!`)` <br /> Set the activity under test. <br /> | ||

## Public constructors

### ActivityInstrumentationTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ActivityInstrumentationTestCase(
    pkg: String!, 
    activityClass: Class<T>!)
```

Creates an [ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md) in non-touch mode.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:ignored - no longer in use. |
| `activityClass` | [Class](../java.lang/Class.md)\<T\>!:The activity to test. This must be a class in the instrumentation targetPackage specified in the AndroidManifest.xml |

### ActivityInstrumentationTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ActivityInstrumentationTestCase(
    pkg: String!, 
    activityClass: Class<T>!, 
    initialTouchMode: Boolean)
```

Creates an [ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md).

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:ignored - no longer in use. |
| `activityClass` | [Class](../java.lang/Class.md)\<T\>!:The activity to test. This must be a class in the instrumentation targetPackage specified in the AndroidManifest.xml |
| `initialTouchMode` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true = in touch mode |
| --- | --- |

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

### testActivityTestCaseSetUpProperly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun testActivityTestCaseSetUpProperly(): Unit
```

**Deprecated:** *Deprecated in Java.*

## Protected methods

### setUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setUp(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### tearDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun tearDown(): Unit
```

**Deprecated:** *Deprecated in Java.*

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |
