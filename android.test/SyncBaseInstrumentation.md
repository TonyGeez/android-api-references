# SyncBaseInstrumentation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncBaseInstrumentation

Kotlin| [Java](https://developer.android.com/reference/android/test/SyncBaseInstrumentation "View this page in Java") 
| --- | --- |

```
open class SyncBaseInstrumentation : InstrumentationTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) ||
| | ↳ | [android.test.SyncBaseInstrumentation](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation#) |

| **This class was deprecated in API level 24.**
|
| Use [InstrumentationRegistry](https://developer.android.com/reference/android/support/test/InstrumentationRegistry.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

If you would like to test sync a single provider with an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase), this provides some of the boiler plate in [setUp](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation#setUp())and [tearDown](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#tearDown()).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SyncBaseInstrumentation](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation#SyncBaseInstrumentation())`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelSyncsandDisableAutoSync](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation#cancelSyncsandDisableAutoSync())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation#setUp())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [syncProvider](https://developer.android.com/reference/kotlin/android/test/SyncBaseInstrumentation#syncProvider(android.net.Uri,%20kotlin.String,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `accountName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Syncs the specified provider. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)! | [getInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#getInstrumentation())`()` <br /> Inheritors can access the instrumentation using this. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInsrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInsrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInstrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | T | [launchActivity](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivity(kotlin.String,%20java.lang.Class,%20android.os.Bundle))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Utility method for launching an activity. The [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) used to launch the Activity is: action = [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) extras = null, unless a custom bundle is provided here All other fields are null or empty. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | T | [launchActivityWithIntent](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivityWithIntent(kotlin.String,%20java.lang.Class,%20android.content.Intent))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` <br /> Utility method for launching an activity with a specific Intent. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTest())`()` <br /> Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), the test is run on the UI thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTestOnUiThread](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTestOnUiThread(java.lang.Runnable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Helper for running portions of a test on the UI thread. Note, in most cases it is simpler to annotate the test method with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), which will run the entire test method on the UI thread. Use this method if you need to switch in and out of the UI thread to perform your test. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. For instance: sendKeys(KEYCODE_DPAD_LEFT, KEYCODE_DPAD_CENTER). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.String))`(`keysSequence:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends a series of key events through instrumentation and waits for idle. The sequence of keys is a string containing the key names as specified in KeyEvent, without the KEYCODE_ prefix. For instance: sendKeys("DPAD_LEFT A B C DPAD_CENTER"). Each key can be repeated by using the N\* prefix. For instance, to send two KEYCODE_DPAD_LEFT, use the following: sendKeys("2\*DPAD_LEFT"). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRepeatedKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendRepeatedKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. Each key code must be preceded by the number of times the key code must be sent. For instance: sendRepeatedKeys(1, KEYCODE_DPAD_CENTER, 2, KEYCODE_DPAD_LEFT). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#tearDown())`()` <br /> Make sure all resources are cleaned up and garbage collected before moving on to the next test. Subclasses that override this method should make sure they call super.tearDown() at the end of the overriding method. <br /> | ||

## Public constructors

### SyncBaseInstrumentation

```
SyncBaseInstrumentation()
```

## Protected methods

### cancelSyncsandDisableAutoSync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun cancelSyncsandDisableAutoSync(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setUp(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### syncProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun syncProvider(
    uri: Uri!, 
    accountName: String!, 
    authority: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Syncs the specified provider.

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |
