# ActivityTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActivityTestCase

Kotlin| [Java](ActivityTestCase.md) 
| --- | --- |

```
abstract class ActivityTestCase : InstrumentationTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.test.InstrumentationTestCase](InstrumentationTestCase.md) ||
| | ↳ | [android.test.ActivityTestCase](ActivityTestCase.md) |

| Known Direct Subclasses [ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md), [ActivityInstrumentationTestCase2](ActivityInstrumentationTestCase2.md), [ActivityUnitTestCase](ActivityUnitTestCase.md) |----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------| | [ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md) | This class provides functional testing of a single activity. | | [ActivityInstrumentationTestCase2](ActivityInstrumentationTestCase2.md) | This class provides functional testing of a single activity. | | [ActivityUnitTestCase](ActivityUnitTestCase.md) | This class provides isolated testing of a single activity. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 24.**
|
| New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This is common code used to support Activity test cases. For more useful classes, please see [android.test.ActivityUnitTestCase](ActivityUnitTestCase.md) and [android.test.ActivityInstrumentationTestCase](ActivityInstrumentationTestCase.md).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [ActivityTestCase](ActivityTestCase.md))`()` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Activity](../android.app/Activity.md)! | [getActivity](ActivityTestCase.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](ActivityTestCase.md))`(`testCaseClass:` ` [Class](../java.lang/Class.md)<*>!`)` This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setActivity](ActivityTestCase.md))`(`testActivity:` ` [Activity](../android.app/Activity.md)!`)` Set the activity under test. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [InstrumentationTestCase](InstrumentationTestCase.md) |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Instrumentation](../android.app/Instrumentation.md)! | [getInstrumentation](InstrumentationTestCase.md))`()` <br /> Inheritors can access the instrumentation using this. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInsrumentation](InstrumentationTestCase.md))`(`instrumentation:` ` [Instrumentation](../android.app/Instrumentation.md)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInstrumentation](InstrumentationTestCase.md))`(`instrumentation:` ` [Instrumentation](../android.app/Instrumentation.md)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | T | [launchActivity](InstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](../java.lang/Class.md)<T>!`, `extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> Utility method for launching an activity. The [Intent](../android.content/Intent.md) used to launch the Activity is: action = [Intent.ACTION_MAIN](../android.content/Intent.md) extras = null, unless a custom bundle is provided here All other fields are null or empty. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | T | [launchActivityWithIntent](InstrumentationTestCase.md))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](../java.lang/Class.md)<T>!`, `intent:` ` [Intent](../android.content/Intent.md)!`)` <br /> Utility method for launching an activity with a specific Intent. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](InstrumentationTestCase.md))`()` <br /> Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](UiThreadTest.md), the test is run on the UI thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTestOnUiThread](InstrumentationTestCase.md))`(`r:` ` [Runnable](../java.lang/Runnable.md)!`)` <br /> Helper for running portions of a test on the UI thread. Note, in most cases it is simpler to annotate the test method with [android.test.UiThreadTest](UiThreadTest.md), which will run the entire test method on the UI thread. Use this method if you need to switch in and out of the UI thread to perform your test. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](InstrumentationTestCase.md))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. For instance: sendKeys(KEYCODE_DPAD_LEFT, KEYCODE_DPAD_CENTER). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](InstrumentationTestCase.md))`(`keysSequence:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends a series of key events through instrumentation and waits for idle. The sequence of keys is a string containing the key names as specified in KeyEvent, without the KEYCODE_ prefix. For instance: sendKeys("DPAD_LEFT A B C DPAD_CENTER"). Each key can be repeated by using the N\* prefix. For instance, to send two KEYCODE_DPAD_LEFT, use the following: sendKeys("2\*DPAD_LEFT"). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRepeatedKeys](InstrumentationTestCase.md))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. Each key code must be preceded by the number of times the key code must be sent. For instance: sendRepeatedKeys(1, KEYCODE_DPAD_CENTER, 2, KEYCODE_DPAD_LEFT). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](InstrumentationTestCase.md))`()` <br /> Make sure all resources are cleaned up and garbage collected before moving on to the next test. Subclasses that override this method should make sure they call super.tearDown() at the end of the overriding method. <br /> | ||

## Public constructors

### ActivityTestCase

```
ActivityTestCase()
```

## Protected methods

### getActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getActivity(): Activity!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------|
| [Activity](../android.app/Activity.md)! | Returns the activity under test. |

### scrubClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun scrubClass(testCaseClass: Class<*>!): Unit
```

**Deprecated:** *Deprecated in Java.*

This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `testCaseClass` | [Class](../java.lang/Class.md)\<\*\>!:The class of the derived TestCase implementation. |

| Exceptions ||
|------------------------------------|---|
| `java.lang.IllegalAccessException` | |

### setActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setActivity(testActivity: Activity!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the activity under test.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------|
| `testActivity` | [Activity](../android.app/Activity.md)!:The activity under test |
