# SingleLaunchActivityTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SingleLaunchActivityTestCase

Kotlin| [Java](SingleLaunchActivityTestCase.md) 
| --- | --- |

```
abstract class SingleLaunchActivityTestCase<T : Activity!> : InstrumentationTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.test.InstrumentationTestCase](InstrumentationTestCase.md) ||
| | ↳ | [android.test.SingleLaunchActivityTestCase](SingleLaunchActivityTestCase.md) |

| **This class was deprecated in API level 24.**
|
| Use [ActivityTestRule](../android/support/test/rule/ActivityTestRule.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

If you would like to test a single activity with an [android.test.InstrumentationTestCase](InstrumentationTestCase.md), this provides some of the boiler plate to launch and finish the activity in [setUp](SingleLaunchActivityTestCase.md))and [tearDown](SingleLaunchActivityTestCase.md)). This launches the activity only once for the entire class instead of doing it in every setup / teardown call.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SingleLaunchActivityTestCase](SingleLaunchActivityTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityClass:` ` [Class](../java.lang/Class.md)<T>!`)` **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openT | [getActivity](SingleLaunchActivityTestCase.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testActivityTestCaseSetUpProperly](SingleLaunchActivityTestCase.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](SingleLaunchActivityTestCase.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](SingleLaunchActivityTestCase.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [InstrumentationTestCase](InstrumentationTestCase.md) |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Instrumentation](../android.app/Instrumentation.md)! | [getInstrumentation](InstrumentationTestCase.md))`()` <br /> Inheritors can access the instrumentation using this. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInsrumentation](InstrumentationTestCase.md))`(`instrumentation:` ` [Instrumentation](../android.app/Instrumentation.md)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInstrumentation](InstrumentationTestCase.md))`(`instrumentation:` ` [Instrumentation](../android.app/Instrumentation.md)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | T | [launchActivity](InstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](../java.lang/Class.md)<T>!`, `extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> Utility method for launching an activity. The [Intent](../android.content/Intent.md) used to launch the Activity is: action = [Intent.ACTION_MAIN](../android.content/Intent.md) extras = null, unless a custom bundle is provided here All other fields are null or empty. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | T | [launchActivityWithIntent](InstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](../java.lang/Class.md)<T>!`, `intent:` ` [Intent](../android.content/Intent.md)!`)` <br /> Utility method for launching an activity with a specific Intent. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](InstrumentationTestCase.md))`()` <br /> Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](UiThreadTest.md), the test is run on the UI thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTestOnUiThread](InstrumentationTestCase.md))`(`r:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> Helper for running portions of a test on the UI thread. Note, in most cases it is simpler to annotate the test method with [android.test.UiThreadTest](UiThreadTest.md), which will run the entire test method on the UI thread. Use this method if you need to switch in and out of the UI thread to perform your test. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](InstrumentationTestCase.md))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. For instance: sendKeys(KEYCODE_DPAD_LEFT, KEYCODE_DPAD_CENTER). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](InstrumentationTestCase.md))`(`keysSequence:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends a series of key events through instrumentation and waits for idle. The sequence of keys is a string containing the key names as specified in KeyEvent, without the KEYCODE_ prefix. For instance: sendKeys("DPAD_LEFT A B C DPAD_CENTER"). Each key can be repeated by using the N\* prefix. For instance, to send two KEYCODE_DPAD_LEFT, use the following: sendKeys("2\*DPAD_LEFT"). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRepeatedKeys](InstrumentationTestCase.md))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. Each key code must be preceded by the number of times the key code must be sent. For instance: sendRepeatedKeys(1, KEYCODE_DPAD_CENTER, 2, KEYCODE_DPAD_LEFT). <br /> | ||

## Public constructors

### SingleLaunchActivityTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SingleLaunchActivityTestCase(
    pkg: String!, 
    activityClass: Class<T>!)
```

**NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package hosting the activity to be launched. |
| `activityClass` | [Class](../java.lang/Class.md)\<T\>!:The activity to test. |

## Public methods

### getActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActivity(): T
```

**Deprecated:** *Deprecated in Java.* 

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
