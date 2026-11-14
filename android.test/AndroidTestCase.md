# AndroidTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AndroidTestCase

Kotlin| [Java](https://developer.android.com/reference/android/test/AndroidTestCase "View this page in Java") 

```
open class AndroidTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.test.AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#) |

| Known Direct Subclasses [ApplicationTestCase](https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase), [LoaderTestCase](https://developer.android.com/reference/kotlin/android/test/LoaderTestCase), [ProviderTestCase2](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2), [ServiceTestCase](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ApplicationTestCase](https://developer.android.com/reference/kotlin/android/test/ApplicationTestCase) | This test case provides a framework in which you can test Application classes in a controlled environment. | | [LoaderTestCase](https://developer.android.com/reference/kotlin/android/test/LoaderTestCase) | A convenience class for testing [Loader](https://developer.android.com/reference/kotlin/android/content/Loader.html#) s. | | [ProviderTestCase2](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2) | This test case class provides a framework for testing a single [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#) and for testing your app code with an isolated content provider. | | [ServiceTestCase](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase) | This test case provides a framework in which you can test Service classes in a controlled environment. | |

| **This class was deprecated in API level 24.**
|
| Use [InstrumentationRegistry](https://developer.android.com/reference/android/support/test/InstrumentationRegistry.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

Extend this if you need to access Resources or other things that depend on Activity Context.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#AndroidTestCase())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertActivityRequiresPermission](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertActivityRequiresPermission(kotlin.String,%20kotlin.String,%20kotlin.String))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown that mentions the permission in its error message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertReadingContentUriRequiresPermission](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertReadingContentUriRequiresPermission(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown mentioning the particular permission. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertWritingContentUriRequiresPermission](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertWritingContentUriRequiresPermission(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown mentioning the particular permission. |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getContext())`()` <br /> |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getTestContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getTestContext())`()` Returns the test context that was set via [setTestContext(android.content.Context)](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testAndroidTestCaseSetupProperly](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#testAndroidTestCaseSetupProperly())`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#scrubClass(java.lang.Class))`(`testCaseClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setUp())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#tearDown())`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [mContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#mContext:android.content.Context) <br /> |

## Public constructors

### AndroidTestCase

```
AndroidTestCase()
```

## Public methods

### assertActivityRequiresPermission

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun assertActivityRequiresPermission(
    packageName: String!, 
    className: String!, 
    permission: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown that mentions the permission in its error message. Note that an instrumentation isn't needed because all we are looking for is a security error and we don't need to wait for the activity to launch and get a handle to the activity.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package name of the activity to launch. |
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The class of the activity to launch. |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the permission. |

### assertReadingContentUriRequiresPermission

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun assertReadingContentUriRequiresPermission(
    uri: Uri!, 
    permission: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown mentioning the particular permission.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The uri that requires a permission to query. |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The permission that should be required. |

### assertWritingContentUriRequiresPermission

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun assertWritingContentUriRequiresPermission(
    uri: Uri!, 
    permission: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown mentioning the particular permission.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:The uri that requires a permission to query. |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The permission that should be required. |

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Context!
```

**Deprecated:** *Deprecated in Java.* 

### getTestContext

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTestContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

Returns the test context that was set via [setTestContext(android.content.Context)](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context)). 

### setContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContext(context: Context!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setTestContext

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTestContext(context: Context!): Unit
```

**Deprecated:** *Deprecated in Java.*

Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. Access to the latter is provided by the context set with the [setContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context))method. 

### testAndroidTestCaseSetupProperly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun testAndroidTestCaseSetupProperly(): Unit
```

**Deprecated:** *Deprecated in Java.*

## Protected methods

### scrubClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun scrubClass(testCaseClass: Class<*>!): Unit
```

**Deprecated:** *Deprecated in Java.*

This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `testCaseClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!:The class of the derived TestCase implementation. |

| Exceptions ||
|------------------------------------|---|
| `java.lang.IllegalAccessException` | |

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

## Properties

### mContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mContext: Context!
```

**Deprecated:** *Deprecated in Java.*
