# AndroidTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AndroidTestCase

Kotlin| [Java](AndroidTestCase.md) 
| --- | --- |

```
open class AndroidTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.AndroidTestCase](AndroidTestCase.md) |

| Known Direct Subclasses [ApplicationTestCase](ApplicationTestCase.md), [LoaderTestCase](LoaderTestCase.md), [ProviderTestCase2](ProviderTestCase2.md), [ServiceTestCase](ServiceTestCase.md) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ApplicationTestCase](ApplicationTestCase.md) | This test case provides a framework in which you can test Application classes in a controlled environment. | | [LoaderTestCase](LoaderTestCase.md) | A convenience class for testing [Loader](../android.content/Loader.md) s. | | [ProviderTestCase2](ProviderTestCase2.md) | This test case class provides a framework for testing a single [ContentProvider](../android.content/ContentProvider.md) and for testing your app code with an isolated content provider. | | [ServiceTestCase](ServiceTestCase.md) | This test case provides a framework in which you can test Service classes in a controlled environment. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 24.**
|
| Use [InstrumentationRegistry](../android/support/test/InstrumentationRegistry.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

Extend this if you need to access Resources or other things that depend on Activity Context.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [AndroidTestCase](AndroidTestCase.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertActivityRequiresPermission](AndroidTestCase.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a [SecurityException](../java.lang/SecurityException.md) is thrown that mentions the permission in its error message. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertReadingContentUriRequiresPermission](AndroidTestCase.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a [SecurityException](../java.lang/SecurityException.md) is thrown mentioning the particular permission. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertWritingContentUriRequiresPermission](AndroidTestCase.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a [SecurityException](../java.lang/SecurityException.md) is thrown mentioning the particular permission. |
| --- | --- |
| open [Context](../android.content/Context.md)! | [getContext](AndroidTestCase.md))`()` <br /> |
| open [Context](../android.content/Context.md)! | [getTestContext](AndroidTestCase.md))`()` Returns the test context that was set via [setTestContext(android.content.Context)](AndroidTestCase.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](AndroidTestCase.md))`(`context:` ` [Context](../android.content/Context.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestContext](AndroidTestCase.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testAndroidTestCaseSetupProperly](AndroidTestCase.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](AndroidTestCase.md))`(`testCaseClass:` ` [Class](../java.lang/Class.md)<*>!`)` This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](AndroidTestCase.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](AndroidTestCase.md))`()` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Context](../android.content/Context.md)! | [mContext](AndroidTestCase.md) <br /> |

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

Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a [SecurityException](../java.lang/SecurityException.md) is thrown that mentions the permission in its error message. Note that an instrumentation isn't needed because all we are looking for is a security error and we don't need to wait for the activity to launch and get a handle to the activity.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The package name of the activity to launch. |
| `className` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The class of the activity to launch. |
| `permission` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the permission. |
| --- | --- |

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

Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a [SecurityException](../java.lang/SecurityException.md) is thrown mentioning the particular permission.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!:The uri that requires a permission to query. |
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

Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a [SecurityException](../java.lang/SecurityException.md) is thrown mentioning the particular permission.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| `uri` | [Uri](../android.net/Uri.md)!:The uri that requires a permission to query. |
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

Returns the test context that was set via [setTestContext(android.content.Context)](AndroidTestCase.md)). 

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

Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. Access to the latter is provided by the context set with the [setContext](AndroidTestCase.md))method. 

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
| `testCaseClass` | [Class](../java.lang/Class.md)\<\*\>!:The class of the derived TestCase implementation. |

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
