Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ApplicationTestCase

Kotlin | [Java](https://developer.android.com/reference/android/test/ApplicationTestCase "View this page in Java")

```
abstract class ApplicationTestCase<T : Application!> : AndroidTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.test.AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase) ||
| | ↳ | [android.test.ApplicationTestCase](https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#) |

> [!CAUTION]
> **This class was deprecated in API level 24.**
>
> Use [InstrumentationRegistry](https://developer.android.com/reference/android/support/test/InstrumentationRegistry.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This test case provides a framework in which you can test Application classes in a controlled environment. It provides basic support for the lifecycle of a Application, and hooks by which you can inject various dependencies and control the environment in which your Application is tested.

**Lifecycle Support.** Every Application is designed to be accessed within a specific sequence of method calls (see `https://developer.android.com/reference/kotlin/android/app/Application.html#` for more details). In order to support the lifecycle of a Application, this test case will make the following calls at the following times.

- The test case will not call onCreate() until your test calls `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#createApplication()`. This gives you a chance to set up or adjust any additional framework or test logic before onCreate().
- After your test completes, the test case `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#tearDown()` method is automatically called, and it will stop \& destroy your application by calling its onDestroy() method.

**Dependency Injection.** Every Application has one inherent dependency, the `https://developer.android.com/reference/kotlin/android/content/Context.html#` in which it runs. This framework allows you to inject a modified, mock, or isolated replacement for this dependencies, and thus perform a true unit test.

If simply run your tests as-is, your Application will be injected with a fully-functional Context. You can create and inject alternative types of Contexts by calling `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context)`. You must do this *before* calling `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#createApplication()`. The test framework provides a number of alternatives for Context, including `https://developer.android.com/reference/kotlin/android/test/mock/MockContext`, `https://developer.android.com/reference/kotlin/android/test/RenamingDelegatingContext`, and `https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#ApplicationTestCase(java.lang.Class)(applicationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>!)` <br /> |

| Public methods ||
|---|---|
| open T | `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#getApplication()()` <br /> |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#getSystemContext()()` Return a real (not mocked or instrumented) system Context that can be used when generating Mock or other Context objects for your Application under test. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#testApplicationTestCaseSetUpProperly()()` This test simply confirms that the Application class can be instantiated properly. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#createApplication()()` Start the Application under test, in the same way as if it was started by the system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#setUp()()` This will do the work to instantiate the Application under test. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#tearDown()()` Shuts down the Application under test. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#terminateApplication()()` This will make the necessary calls to terminate the Application under test (it will call onTerminate(). |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertActivityRequiresPermission(kotlin.String,%20kotlin.String,%20kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, className: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown that mentions the permission in its error message. Note that an instrumentation isn't needed because all we are looking for is a security error and we don't need to wait for the activity to launch and get a handle to the activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertReadingContentUriRequiresPermission(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown mentioning the particular permission. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertWritingContentUriRequiresPermission(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown mentioning the particular permission. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getContext()()` <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getTestContext()()` Returns the test context that was set via `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#scrubClass(java.lang.Class)(testCaseClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!)` This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. Access to the latter is provided by the context set with the `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context)` method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#testAndroidTestCaseSetupProperly()()` <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase` |---|---| | `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#mContext:android.content.Context` <br /> | ||

## Public constructors

### ApplicationTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ApplicationTestCase(applicationClass: Class<T>!)
```

## Public methods

### getApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getApplication(): T
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|---|
| `T` | Returns the actual Application under test. |

### getSystemContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSystemContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

Return a real (not mocked or instrumented) system Context that can be used when generating Mock or other Context objects for your Application under test.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | Returns a reference to a normal Context. |

### testApplicationTestCaseSetUpProperly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun testApplicationTestCaseSetUpProperly(): Unit
```

**Deprecated:** *Deprecated in Java.*

This test simply confirms that the Application class can be instantiated properly.

| Exceptions ||
|---|---|
| `java.lang.Exception` | |

## Protected methods

### createApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun createApplication(): Unit
```

**Deprecated:** *Deprecated in Java.*

Start the Application under test, in the same way as if it was started by the system. If you use this method to start the Application, it will automatically be stopped by `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#tearDown()`. If you wish to inject a specialized Context for your test, by calling `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context)`, you must do so before calling this method.

### setUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun setUp(): Unit
```

**Deprecated:** *Deprecated in Java.*

This will do the work to instantiate the Application under test. After this, your test code must also start and stop the Application.

### tearDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun tearDown(): Unit
```

**Deprecated:** *Deprecated in Java.*

Shuts down the Application under test. Also makes sure all resources are cleaned up and garbage collected before moving on to the next test. Subclasses that override this method should make sure they call super.tearDown() at the end of the overriding method.

| Exceptions ||
|---|---|
| `java.lang.Exception` | |

### terminateApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun terminateApplication(): Unit
```

**Deprecated:** *Deprecated in Java.*

This will make the necessary calls to terminate the Application under test (it will call onTerminate(). Ordinarily this will be called automatically (by `https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase#tearDown()`, but you can call it directly from your test in order to check for proper shutdown behaviors.
