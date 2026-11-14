Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoaderTestCase

Kotlin | [Java](../android/test/LoaderTestCase.md)
| --- | --- |

```
open class LoaderTestCase : AndroidTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.test.AndroidTestCase](../android/test/AndroidTestCase.md) ||
| | ↳ | [android.test.LoaderTestCase](../android/test/LoaderTestCase.md) |

A convenience class for testing `https://developer.android.com/reference/kotlin/android/content/Loader.html#`s. This test case provides a simple way to synchronously get the result from a Loader making it easy to assert that the Loader returns the expected result.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/test/LoaderTestCase#LoaderTestCase()()` <br /> |

| Public methods ||
|---|---|
| open T | `https://developer.android.com/reference/kotlin/android/test/LoaderTestCase#getLoaderResultSynchronously(android.content.Loader)(loader: https://developer.android.com/reference/kotlin/android/content/Loader.html#<T>!)` Runs a Loader synchronously and returns the result of the load. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertActivityRequiresPermission(kotlin.String,%20kotlin.String,%20kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, className: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown that mentions the permission in its error message. Note that an instrumentation isn't needed because all we are looking for is a security error and we don't need to wait for the activity to launch and get a handle to the activity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertReadingContentUriRequiresPermission(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown mentioning the particular permission. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertWritingContentUriRequiresPermission(android.net.Uri,%20kotlin.String)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, permission: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` is thrown mentioning the particular permission. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getContext()()` <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getTestContext()()` Returns the test context that was set via `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#scrubClass(java.lang.Class)(testCaseClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!)` This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. Access to the latter is provided by the context set with the `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context)` method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setUp()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#tearDown()()` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#testAndroidTestCaseSetupProperly()()` <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase` |---|---| | `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | `https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#mContext:android.content.Context` <br /> | ||

## Public constructors

### LoaderTestCase

```
LoaderTestCase()
```

## Public methods

### getLoaderResultSynchronously

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Any!> getLoaderResultSynchronously(loader: Loader<T>!): T
```

Runs a Loader synchronously and returns the result of the load. The loader will be started, stopped, and destroyed by this method so it cannot be reused.

| Parameters ||
|---|---|
| `loader` | [Loader](../android/content/Loader.md)\<T\>!: The loader to run synchronously |

| Return ||
|---|---|
| `T` | The result from the loader |
