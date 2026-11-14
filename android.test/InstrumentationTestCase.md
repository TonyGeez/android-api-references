# InstrumentationTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstrumentationTestCase

Kotlin| [Java](https://developer.android.com/reference/android/test/InstrumentationTestCase "View this page in Java") 

```
open class InstrumentationTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#) |

| Known Direct Subclasses [ActivityTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase), [ProviderTestCase](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase), [SingleLaunchActivityTestCase](https://developer.android.com/reference/kotlin/android/test/SingleLaunchActivityTestCase), [SyncBaseInstrumentation](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation) |--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ActivityTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityTestCase) | This is common code used to support Activity test cases. | | [ProviderTestCase](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase) | If you would like to test a single content provider with an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#), this provides some of the boiler plate in [setUp](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#setUp())and [tearDown](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#tearDown()). | | [SingleLaunchActivityTestCase](https://developer.android.com/reference/kotlin/android/test/SingleLaunchActivityTestCase) | If you would like to test a single activity with an [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#), this provides some of the boiler plate to launch and finish the activity in [setUp](https://developer.android.com/reference/kotlin/android/test/SingleLaunchActivityTestCase#setUp())and [tearDown](https://developer.android.com/reference/kotlin/android/test/SingleLaunchActivityTestCase#tearDown()). | | [SyncBaseInstrumentation](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation) | If you would like to test sync a single provider with an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#), this provides some of the boiler plate in [setUp](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation#setUp())and [tearDown](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#tearDown()). | |

| Known Indirect Subclasses [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase), [ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), [ActivityUnitTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase) |----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------| | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) | This class provides functional testing of a single activity. | | [ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2) | This class provides functional testing of a single activity. | | [ActivityUnitTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityUnitTestCase) | This class provides isolated testing of a single activity. | |

| **This class was deprecated in API level 24.**
|
| Use [InstrumentationRegistry](https://developer.android.com/reference/androidx/test/platform/app/InstrumentationRegistry.html) instead. New tests should be written using the [AndroidX Test Library](https://developer.android.com/training/testing/index.html).

A test case that has access to [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#InstrumentationTestCase())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)! | [getInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#getInstrumentation())`()` Inheritors can access the instrumentation using this. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInsrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInsrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` Injects instrumentation into this test case. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInstrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` Injects instrumentation into this test case. |
| T | [launchActivity](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivity(kotlin.String,%20java.lang.Class,%20android.os.Bundle))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Utility method for launching an activity. |
| T | [launchActivityWithIntent](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivityWithIntent(kotlin.String,%20java.lang.Class,%20android.content.Intent))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Utility method for launching an activity with a specific Intent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTestOnUiThread](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTestOnUiThread(java.lang.Runnable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Helper for running portions of a test on the UI thread. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sends a series of key events through instrumentation and waits for idle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.String))`(`keysSequence:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sends a series of key events through instrumentation and waits for idle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRepeatedKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendRepeatedKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sends a series of key events through instrumentation and waits for idle. |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTest())`()` Runs the current unit test. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#tearDown())`()` Make sure all resources are cleaned up and garbage collected before moving on to the next test. |

## Public constructors

### InstrumentationTestCase

```
InstrumentationTestCase()
```

## Public methods

### getInstrumentation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInstrumentation(): Instrumentation!
```

**Deprecated:** *Deprecated in Java.*

Inheritors can access the instrumentation using this.

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------|
| [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)! | instrumentation |

### injectInsrumentation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun injectInsrumentation(instrumentation: Instrumentation!): Unit
```

**Deprecated:** *Incorrect spelling, use [injectInstrumentation(android.app.Instrumentation)](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInstrumentation(android.app.Instrumentation))instead.*

Injects instrumentation into this test case. This method is called by the test runner during test setup.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `instrumentation` | [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!:the instrumentation to use with this instance |

### injectInstrumentation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun injectInstrumentation(instrumentation: Instrumentation!): Unit
```

**Deprecated:** *Deprecated in Java.*

Injects instrumentation into this test case. This method is called by the test runner during test setup.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `instrumentation` | [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!:the instrumentation to use with this instance |

### launchActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Activity!> launchActivity(
    pkg: String!, 
    activityCls: Class<T>!, 
    extras: Bundle!
): T
```

**Deprecated:** *Deprecated in Java.*

Utility method for launching an activity.

The [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) used to launch the Activity is: action = [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) extras = null, unless a custom bundle is provided here All other fields are null or empty.

**NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package hosting the activity to be launched. |
| `activityCls` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:The activity class to launch. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:Optional extra stuff to pass to the activity. |

| Return ||
|---|----------------------------------------|
| T | The activity, or null if non launched. |

### launchActivityWithIntent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Activity!> launchActivityWithIntent(
    pkg: String!, 
    activityCls: Class<T>!, 
    intent: Intent!
): T
```

**Deprecated:** *Deprecated in Java.*

Utility method for launching an activity with a specific Intent.

**NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------|
| `pkg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package hosting the activity to be launched. |
| `activityCls` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:The activity class to launch. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent to launch with |

| Return ||
|---|----------------------------------------|
| T | The activity, or null if non launched. |

### runTestOnUiThread

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun runTestOnUiThread(r: Runnable!): Unit
```

**Deprecated:** *Deprecated in Java.*

Helper for running portions of a test on the UI thread. Note, in most cases it is simpler to annotate the test method with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), which will run the entire test method on the UI thread. Use this method if you need to switch in and out of the UI thread to perform your test.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:runnable containing test code in the [Runnable.run()](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#run())method |

### sendKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendKeys(vararg keys: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sends a series of key events through instrumentation and waits for idle. For instance: sendKeys(KEYCODE_DPAD_LEFT, KEYCODE_DPAD_CENTER).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `keys` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The series of key codes to send through instrumentation. |

### sendKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendKeys(keysSequence: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sends a series of key events through instrumentation and waits for idle. The sequence of keys is a string containing the key names as specified in KeyEvent, without the KEYCODE_ prefix. For instance: sendKeys("DPAD_LEFT A B C DPAD_CENTER"). Each key can be repeated by using the N\* prefix. For instance, to send two KEYCODE_DPAD_LEFT, use the following: sendKeys("2\*DPAD_LEFT").

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------|
| `keysSequence` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The sequence of keys. |

### sendRepeatedKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendRepeatedKeys(vararg keys: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sends a series of key events through instrumentation and waits for idle. Each key code must be preceded by the number of times the key code must be sent. For instance: sendRepeatedKeys(1, KEYCODE_DPAD_CENTER, 2, KEYCODE_DPAD_LEFT).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `keys` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The series of key repeats and codes to send through instrumentation. |

## Protected methods

### runTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun runTest(): Unit
```

**Deprecated:** *Deprecated in Java.*

Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), the test is run on the UI thread. 

### tearDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun tearDown(): Unit
```

**Deprecated:** *Deprecated in Java.*

Make sure all resources are cleaned up and garbage collected before moving on to the next test. Subclasses that override this method should make sure they call super.tearDown() at the end of the overriding method.

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |
