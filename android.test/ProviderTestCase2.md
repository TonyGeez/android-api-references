# ProviderTestCase2

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProviderTestCase2

Kotlin| [Java](https://developer.android.com/reference/android/test/ProviderTestCase2 "View this page in Java") 

```
abstract class ProviderTestCase2<T : ContentProvider!> : AndroidTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.test.AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase) ||
| | ↳ | [android.test.ProviderTestCase2](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#) |

This test case class provides a framework for testing a single [ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#) and for testing your app code with an isolated content provider. Instead of using the system map of providers that is based on the manifests of other applications, the test case creates its own internal map. It then uses this map to resolve providers given an authority. This allows you to inject test providers and to null out providers that you do not want to use.

This test case also sets up the following mock objects:

- An [android.test.IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext) that stubs out Context methods that might affect the rest of the running system, while allowing tests to do real file and database work.
- A [android.test.mock.MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver) that provides the functionality of a regular content resolver, but uses [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext). It stubs out android.content.ContentResolver#notifyChange(Uri,ContentObserver,boolean) to prevent the test from affecting the running system.
- An instance of the provider under test, running in an [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext).

This framework is set up automatically by the base class' [setUp()](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#setUp())method. If you override this method, you must call the super method as the first statement in your override.

In order for their tests to be run, concrete subclasses must provide their own constructor with no arguments. This constructor must call [ProviderTestCase2(java.lang.Class,java.lang.String)](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#ProviderTestCase2(java.lang.Class,%20kotlin.String))as its first operation.
For more information on content provider testing, please see [Content Provider Testing](https://developer.android.com/tools/testing/contentprovider_testing.html).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ProviderTestCase2](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#ProviderTestCase2(java.lang.Class,%20kotlin.String))`(`providerClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `providerAuthority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver)! | [getMockContentResolver](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#getMockContentResolver())`()` Gets the [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver) created by this class during initialization. |
| open [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext)! | [getMockContext](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#getMockContext())`()` Gets the [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext) created by this class during initialization. |
| openT | [getProvider](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#getProvider())`()` Returns the content provider created by this class in the [setUp()](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#setUp())method. |
| openstatic [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)! | [newResolverWithContentProviderFromSql](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#newResolverWithContentProviderFromSql(android.content.Context,%20kotlin.String,%20java.lang.Class,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String))`(`targetContext:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `filenamePrefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `providerClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `databaseVersion:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sql:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new content provider of the same type as that passed to the test case class, with an authority name set to the authority parameter, and using an SQLite database as the underlying data source. |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#setUp())`()` Sets up the environment for the test fixture. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#tearDown())`()` Tears down the environment for the test fixture. |

| Inherited functions ||
|---|---|
| From class [AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertActivityRequiresPermission](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertActivityRequiresPermission(kotlin.String,%20kotlin.String,%20kotlin.String))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown that mentions the permission in its error message. Note that an instrumentation isn't needed because all we are looking for is a security error and we don't need to wait for the activity to launch and get a handle to the activity. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertReadingContentUriRequiresPermission](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertReadingContentUriRequiresPermission(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown mentioning the particular permission. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertWritingContentUriRequiresPermission](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertWritingContentUriRequiresPermission(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown mentioning the particular permission. <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getContext())`()` <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getTestContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getTestContext())`()` <br /> Returns the test context that was set via [setTestContext(android.content.Context)](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#scrubClass(java.lang.Class))`(`testCaseClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` <br /> This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. Access to the latter is provided by the context set with the [setContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context))method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testAndroidTestCaseSetupProperly](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#testAndroidTestCaseSetupProperly())`()` <br /> | ||

| Inherited properties ||
|---|---|
| From class [AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------| | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [mContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#mContext:android.content.Context) <br /> | ||

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
| `providerClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:The class name of the provider under test |
| `providerAuthority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The provider's authority string |

## Public methods

### getMockContentResolver

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMockContentResolver(): MockContentResolver!
```

Gets the [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver) created by this class during initialization. You must use the methods of this resolver to access the provider under test.

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver)! | A [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver) instance. |

### getMockContext

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMockContext(): IsolatedContext!
```

Gets the [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext) created by this class during initialization.

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext)! | The [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext) instance |

### getProvider

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProvider(): T
```

Returns the content provider created by this class in the [setUp()](https://developer.android.com/reference/kotlin/android/test/ProviderTestCase2#setUp())method.

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

Creates a new content provider of the same type as that passed to the test case class, with an authority name set to the authority parameter, and using an SQLite database as the underlying data source. The SQL statement parameter is used to create the database. This method also creates a new [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver) and adds the provider to it.

Both the new provider and the new resolver are put into an [IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext) that uses the targetContext parameter for file operations and a [MockContext](https://developer.android.com/reference/kotlin/android/test/mock/MockContext) for everything else. The IsolatedContext prepends the filenamePrefix parameter to file, database, and directory names.

This is a convenience method for creating a "mock" provider that can contain test data.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `targetContext` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context to use as the basis of the IsolatedContext |
| `filenamePrefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string that is prepended to file, database, and directory names |
| `providerClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:The type of the provider being tested |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The authority string to associated with the test provider |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name assigned to the database |
| `databaseVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The version assigned to the database |
| `sql` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string containing the SQL statements that are needed to create the desired database and its tables. The format is the same as that generated by the [sqlite3](http://www.sqlite.org/sqlite.html) tool's`.dump`command. |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ContentResolver](https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#)! | ContentResolver A new [MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver) linked to the provider |

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

Creates a new [android.test.mock.MockContentResolver](https://developer.android.com/reference/kotlin/android/test/mock/MockContentResolver), a new IsolatedContext that isolates the provider's file operations, and a new instance of the provider under test within the isolated environment.

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |

### tearDown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun tearDown(): Unit
```

Tears down the environment for the test fixture.

Calls [android.content.ContentProvider#shutdown()](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#shutdown())on the [android.content.ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#) represented by mProvider.
