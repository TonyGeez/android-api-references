# ProviderTestCase2

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProviderTestCase2

Kotlin| [Java](ProviderTestCase2.md) 
| --- | --- |

```
abstract class ProviderTestCase2<T : ContentProvider!> : AndroidTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.test.AndroidTestCase](AndroidTestCase.md) ||
| | ↳ | [android.test.ProviderTestCase2](ProviderTestCase2.md) |

This test case class provides a framework for testing a single [ContentProvider](../android.content/ContentProvider.md) and for testing your app code with an isolated content provider. Instead of using the system map of providers that is based on the manifests of other applications, the test case creates its own internal map. It then uses this map to resolve providers given an authority. This allows you to inject test providers and to null out providers that you do not want to use.

This test case also sets up the following mock objects:

- An [android.test.IsolatedContext](IsolatedContext.md) that stubs out Context methods that might affect the rest of the running system, while allowing tests to do real file and database work.
- A [android.test.mock.MockContentResolver](../android.test.mock/MockContentResolver.md) that provides the functionality of a regular content resolver, but uses [IsolatedContext](IsolatedContext.md). It stubs out android.content.ContentResolver#notifyChange(Uri,ContentObserver,boolean) to prevent the test from affecting the running system.
- An instance of the provider under test, running in an [IsolatedContext](IsolatedContext.md).

This framework is set up automatically by the base class' [setUp()](ProviderTestCase2.md))method. If you override this method, you must call the super method as the first statement in your override.

In order for their tests to be run, concrete subclasses must provide their own constructor with no arguments. This constructor must call [ProviderTestCase2(java.lang.Class,java.lang.String)](ProviderTestCase2.md))as its first operation.
For more information on content provider testing, please see [Content Provider Testing](https://developer.android.com/tools/testing/contentprovider_testing.html).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProviderTestCase2](ProviderTestCase2.md))`(`providerClass:` ` [Class](../java.lang/Class.md)<T>!`, `providerAuthority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MockContentResolver](../android.test.mock/MockContentResolver.md)! | [getMockContentResolver](ProviderTestCase2.md))`()` Gets the [MockContentResolver](../android.test.mock/MockContentResolver.md) created by this class during initialization. |
| open [IsolatedContext](IsolatedContext.md)! | [getMockContext](ProviderTestCase2.md))`()` Gets the [IsolatedContext](IsolatedContext.md) created by this class during initialization. |
| openT | [getProvider](ProviderTestCase2.md))`()` Returns the content provider created by this class in the [setUp()](ProviderTestCase2.md))method. |
| --- | --- |
| openstatic [ContentResolver](../android.content/ContentResolver.md)! | [newResolverWithContentProviderFromSql](ProviderTestCase2.md))`(`targetContext:` ` [Context](../android.content/Context.md)!`, `filenamePrefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `providerClass:` ` [Class](../java.lang/Class.md)<T>!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `databaseVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new content provider of the same type as that passed to the test case class, with an authority name set to the authority parameter, and using an SQLite database as the underlying data source. |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](ProviderTestCase2.md))`()` Sets up the environment for the test fixture. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](ProviderTestCase2.md))`()` Tears down the environment for the test fixture. |

| Inherited functions ||
|---|---|
| From class [AndroidTestCase](AndroidTestCase.md) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertActivityRequiresPermission](AndroidTestCase.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a [SecurityException](../java.lang/SecurityException.md) is thrown that mentions the permission in its error message. Note that an instrumentation isn't needed because all we are looking for is a security error and we don't need to wait for the activity to launch and get a handle to the activity. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertReadingContentUriRequiresPermission](AndroidTestCase.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a [SecurityException](../java.lang/SecurityException.md) is thrown mentioning the particular permission. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertWritingContentUriRequiresPermission](AndroidTestCase.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a [SecurityException](../java.lang/SecurityException.md) is thrown mentioning the particular permission. <br /> | | [Context](../android.content/Context.md)! | [getContext](AndroidTestCase.md))`()` <br /> | | [Context](../android.content/Context.md)! | [getTestContext](AndroidTestCase.md))`()` <br /> Returns the test context that was set via [setTestContext(android.content.Context)](AndroidTestCase.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](AndroidTestCase.md))`(`testCaseClass:` ` [Class](../java.lang/Class.md)<*>!`)` <br /> This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](AndroidTestCase.md))`(`context:` ` [Context](../android.content/Context.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestContext](AndroidTestCase.md))`(`context:` ` [Context](../android.content/Context.md)!`)` <br /> Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. Access to the latter is provided by the context set with the [setContext](AndroidTestCase.md))method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testAndroidTestCaseSetupProperly](AndroidTestCase.md))`()` <br /> | ||

| Inherited properties ||
|---|---|
| From class [AndroidTestCase](AndroidTestCase.md) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------| | [Context](../android.content/Context.md)! | [mContext](AndroidTestCase.md) <br /> | ||

## Public constructors

### ProviderTestCase2

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProviderTestCase2(
    providerClass: Class<T>!, 
    providerAuthority: String!)
```

Constructor.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `providerClass` | [Class](../java.lang/Class.md)\<T\>!:The class name of the provider under test |
| `providerAuthority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The provider's authority string |

## Public methods

### getMockContentResolver

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMockContentResolver(): MockContentResolver!
```

Gets the [MockContentResolver](../android.test.mock/MockContentResolver.md) created by this class during initialization. You must use the methods of this resolver to access the provider under test.

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [MockContentResolver](../android.test.mock/MockContentResolver.md)! | A [MockContentResolver](../android.test.mock/MockContentResolver.md) instance. |

### getMockContext

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMockContext(): IsolatedContext!
```

Gets the [IsolatedContext](IsolatedContext.md) created by this class during initialization.

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [IsolatedContext](IsolatedContext.md)! | The [IsolatedContext](IsolatedContext.md) instance |

### getProvider

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvider(): T
```

Returns the content provider created by this class in the [setUp()](ProviderTestCase2.md))method.

| Return ||
|---|----------------------------------------------------------------------------------|
| T | T An instance of the provider class given as a parameter to the test case class. |

### newResolverWithContentProviderFromSql

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : ContentProvider!> newResolverWithContentProviderFromSql(
    targetContext: Context!, 
    filenamePrefix: String!, 
    providerClass: Class<T>!, 
    authority: String!, 
    databaseName: String!, 
    databaseVersion: Int, 
    sql: String!
): ContentResolver!
```

Creates a new content provider of the same type as that passed to the test case class, with an authority name set to the authority parameter, and using an SQLite database as the underlying data source. The SQL statement parameter is used to create the database. This method also creates a new [MockContentResolver](../android.test.mock/MockContentResolver.md) and adds the provider to it.

Both the new provider and the new resolver are put into an [IsolatedContext](IsolatedContext.md) that uses the targetContext parameter for file operations and a [MockContext](../android.test.mock/MockContext.md) for everything else. The IsolatedContext prepends the filenamePrefix parameter to file, database, and directory names.

This is a convenience method for creating a "mock" provider that can contain test data.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `targetContext` | [Context](../android.content/Context.md)!:The context to use as the basis of the IsolatedContext |
| `filenamePrefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string that is prepended to file, database, and directory names |
| `providerClass` | [Class](../java.lang/Class.md)\<T\>!:The type of the provider being tested |
| --- | --- |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The authority string to associated with the test provider |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name assigned to the database |
| `databaseVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The version assigned to the database |
| --- | --- |
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string containing the SQL statements that are needed to create the desired database and its tables. The format is the same as that generated by the [sqlite3](http://www.sqlite.org/sqlite.html) tool's`.dump`command. |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentResolver](../android.content/ContentResolver.md)! | ContentResolver A new [MockContentResolver](../android.test.mock/MockContentResolver.md) linked to the provider |

| Exceptions ||
|------------------------------------|---|
| `java.lang.IllegalAccessException` | |
| `java.lang.InstantiationException` | |

## Protected methods

### setUp

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setUp(): Unit
```

Sets up the environment for the test fixture.

Creates a new [android.test.mock.MockContentResolver](../android.test.mock/MockContentResolver.md), a new IsolatedContext that isolates the provider's file operations, and a new instance of the provider under test within the isolated environment.

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |

### tearDown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun tearDown(): Unit
```

Tears down the environment for the test fixture.

Calls [android.content.ContentProvider#shutdown()](../android.content/ContentProvider.md))on the [android.content.ContentProvider](../android.content/ContentProvider.md) represented by mProvider.
