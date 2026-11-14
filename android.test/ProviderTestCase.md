# ProviderTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProviderTestCase

Kotlin| [Java](https://developer.android.com/reference/android/test/ProviderTestCase "View this page in Java") 
| --- | --- |

```
abstract class ProviderTestCase<T : ContentProvider!> : InstrumentationTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) ||
| | ↳ | [android.test.ProviderTestCase](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#) |

| **This class was deprecated in API level 5.**
|
| this class extends InstrumentationTestCase but should extend AndroidTestCase. Use ProviderTestCase2, which corrects this problem, instead.

If you would like to test a single content provider with an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase), this provides some of the boiler plate in [setUp](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#setUp())and [tearDown](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#tearDown()).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProviderTestCase](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#ProviderTestCase(java.lang.Class,%20kotlin.String))`(`providerClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `providerAuthority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver)! | [getMockContentResolver](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#getMockContentResolver())`()` <br /> |
| open [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext)! | [getMockContext](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#getMockContext())`()` <br /> |
| openT | [getProvider](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#getProvider())`()` <br /> |
| --- | --- |
| openstatic [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)! | [newResolverWithContentProviderFromSql](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#newResolverWithContentProviderFromSql(android.content.Context,%20java.lang.Class,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String))`(`targetContext:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `providerClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `databaseVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#setUp())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase#tearDown())`()` Tears down the environment for the test fixture. |

| Inherited functions ||
|---|---|
| From class [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)! | [getInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#getInstrumentation())`()` <br /> Inheritors can access the instrumentation using this. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInsrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInsrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [injectInstrumentation](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#injectInstrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> Injects instrumentation into this test case. This method is called by the test runner during test setup. <br /> | | T | [launchActivity](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivity(kotlin.String,%20java.lang.Class,%20android.os.Bundle))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Utility method for launching an activity. The [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) used to launch the Activity is: action = [Intent.ACTION_MAIN](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MAIN:kotlin.String) extras = null, unless a custom bundle is provided here All other fields are null or empty. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | T | [launchActivityWithIntent](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#launchActivityWithIntent(kotlin.String,%20java.lang.Class,%20android.content.Intent))`(`pkg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `activityCls:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` <br /> Utility method for launching an activity with a specific Intent. **NOTE:** The parameter*pkg*must refer to the package identifier of the package hosting the activity to be launched, which is specified in the AndroidManifest.xml file. This is not necessarily the same as the java package name. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTest())`()` <br /> Runs the current unit test. If the unit test is annotated with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), the test is run on the UI thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTestOnUiThread](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#runTestOnUiThread(java.lang.Runnable))`(`r:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` <br /> Helper for running portions of a test on the UI thread. Note, in most cases it is simpler to annotate the test method with [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest), which will run the entire test method on the UI thread. Use this method if you need to switch in and out of the UI thread to perform your test. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. For instance: sendKeys(KEYCODE_DPAD_LEFT, KEYCODE_DPAD_CENTER). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendKeys(kotlin.String))`(`keysSequence:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sends a series of key events through instrumentation and waits for idle. The sequence of keys is a string containing the key names as specified in KeyEvent, without the KEYCODE_ prefix. For instance: sendKeys("DPAD_LEFT A B C DPAD_CENTER"). Each key can be repeated by using the N\* prefix. For instance, to send two KEYCODE_DPAD_LEFT, use the following: sendKeys("2\*DPAD_LEFT"). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendRepeatedKeys](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase#sendRepeatedKeys(kotlin.Int))`(`vararg` `keys:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sends a series of key events through instrumentation and waits for idle. Each key code must be preceded by the number of times the key code must be sent. For instance: sendRepeatedKeys(1, KEYCODE_DPAD_CENTER, 2, KEYCODE_DPAD_LEFT). <br /> | ||

## Public constructors

### ProviderTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProviderTestCase(
    providerClass: Class<T>!, 
    providerAuthority: String!)
```

## Public methods

### getMockContentResolver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMockContentResolver(): MockContentResolver!
```

**Deprecated:** *Deprecated in Java.* 

### getMockContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMockContext(): IsolatedContext!
```

**Deprecated:** *Deprecated in Java.* 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvider(): T
```

**Deprecated:** *Deprecated in Java.* 

### newResolverWithContentProviderFromSql

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : ContentProvider!> newResolverWithContentProviderFromSql(
    targetContext: Context!, 
    providerClass: Class<T>!, 
    authority: String!, 
    databaseName: String!, 
    databaseVersion: Int, 
    sql: String!
): ContentResolver!
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

Tears down the environment for the test fixture.

Calls [android.content.ContentProvider#shutdown()](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#shutdown())on the [android.content.ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#) represented by mProvider.

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |
