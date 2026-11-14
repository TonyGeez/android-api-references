# ServiceTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceTestCase

Kotlin| [Java](ServiceTestCase.md) 
| --- | --- |

```
abstract class ServiceTestCase<T : Service!> : AndroidTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.test.AndroidTestCase](AndroidTestCase.md) ||
| | ↳ | [android.test.ServiceTestCase](ServiceTestCase.md) |

| **This class was deprecated in API level 24.**
|
| Use [ServiceTestRule](../android/support/test/rule/ServiceTestRule.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This test case provides a framework in which you can test Service classes in a controlled environment. It provides basic support for the lifecycle of a Service, and hooks with which you can inject various dependencies and control the environment in which your Service is tested.
|
| ### Developer Guides
|
| For more information about application testing, read the [Testing](https://developer.android.com/guide/topics/testing/index.html) developer guide.

<br />

**Lifecycle Support.** A Service is accessed with a specific sequence of calls, as described in the [Services](http://developer.android.com/guide/topics/fundamentals/services.html) document. In order to support the lifecycle of a Service,`ServiceTestCase`enforces this protocol:

- The [setUp()](ServiceTestCase.md))method is called before each test method. The base implementation gets the system context. If you override`setUp()`, you must call`super.setUp()`as the first statement in your override.
- The test case waits to call [android.app.Service#onCreate()](../android.app/Service.md))until one of your test methods calls [startService](ServiceTestCase.md))or [bindService](ServiceTestCase.md)). This gives you an opportunity to set up or adjust any additional framework or test logic before you test the running service.
- When one of your test methods calls [ServiceTestCase.startService()](ServiceTestCase.md))or [ServiceTestCase.bindService()](ServiceTestCase.md)), the test case calls [Service.onCreate()](../android.app/Service.md))and then calls either [Service.startService(Intent)](../android.content/ContextWrapper.md))or android.app.Service#bindService(Intent, ServiceConnection, int), as appropriate. It also stores values needed to track and support the lifecycle.
- After each test method finishes, the test case calls the [tearDown](ServiceTestCase.md))method. This method stops and destroys the service with the appropriate calls, depending on how the service was started. If you override`tearDown()`, your must call the`super.tearDown()`as the last statement in your override.

**Dependency Injection.** A service has two inherent dependencies, its [Context](../android.content/Context.md) and its associated [Application](../android.app/Application.md). The ServiceTestCase framework allows you to inject modified, mock, or isolated replacements for these dependencies, and thus perform unit tests with controlled dependencies in an isolated environment.

By default, the test case is injected with a full system context and a generic [MockApplication](../android.test.mock/MockApplication.md) object. You can inject alternatives to either of these by invoking [setContext()](AndroidTestCase.md))or [setApplication()](ServiceTestCase.md)). You must do this*before* calling startService() or bindService(). The test framework provides a number of alternatives for Context, including [MockContext](../android.test.mock/MockContext.md), [RenamingDelegatingContext](RenamingDelegatingContext.md), [ContextWrapper](../android.content/ContextWrapper.md), and [android.test.IsolatedContext](IsolatedContext.md).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServiceTestCase](ServiceTestCase.md))`(`serviceClass:` ` [Class](../java.lang/Class.md)<T>!`)` Constructor |

| Public methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Application](../android.app/Application.md)! | [getApplication](ServiceTestCase.md))`()` Returns the Application object in use by the service under test. |
| openT | [getService](ServiceTestCase.md))`()` <br /> |
| open [Context](../android.content/Context.md)! | [getSystemContext](ServiceTestCase.md))`()` Returns the real system context that is saved by [setUp()](ServiceTestCase.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setApplication](ServiceTestCase.md))`(`application:` ` [Application](../android.app/Application.md)!`)` Sets the application that is used during the test. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testServiceTestCaseSetUpProperly](ServiceTestCase.md))`()` Tests that [setupService()](ServiceTestCase.md))runs correctly and issues an junit. |

| Protected methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IBinder](../android.os/IBinder.md)! | [bindService](ServiceTestCase.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`)` Starts the service under test, in the same way as if it were started by android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](ServiceTestCase.md))`()` Gets the current system context and stores it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupService](ServiceTestCase.md))`()` Creates the service under test and attaches all injected dependencies (Context, Application) to it. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownService](ServiceTestCase.md))`()` Makes the necessary calls to stop (or unbind) the service under test, and calls onDestroy(). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startService](ServiceTestCase.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`)` Starts the service under test, in the same way as if it were started by [Context.startService(Intent)](../android.content/Context.md))with an [android.content.Intent](../android.content/Intent.md) that identifies a service. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](ServiceTestCase.md))`()` Shuts down the service under test. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AndroidTestCase](AndroidTestCase.md) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertActivityRequiresPermission](AndroidTestCase.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a [SecurityException](../java.lang/SecurityException.md) is thrown that mentions the permission in its error message. Note that an instrumentation isn't needed because all we are looking for is a security error and we don't need to wait for the activity to launch and get a handle to the activity. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertReadingContentUriRequiresPermission](AndroidTestCase.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a [SecurityException](../java.lang/SecurityException.md) is thrown mentioning the particular permission. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertWritingContentUriRequiresPermission](AndroidTestCase.md))`(`uri:` ` [Uri](../android.net/Uri.md)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a [SecurityException](../java.lang/SecurityException.md) is thrown mentioning the particular permission. <br /> | | [Context](../android.content/Context.md)! | [getContext](AndroidTestCase.md))`()` <br /> | | [Context](../android.content/Context.md)! | [getTestContext](AndroidTestCase.md))`()` <br /> Returns the test context that was set via [setTestContext(android.content.Context)](AndroidTestCase.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](AndroidTestCase.md))`(`testCaseClass:` ` [Class](../java.lang/Class.md)<*>!`)` <br /> This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](AndroidTestCase.md))`(`context:` ` [Context](../android.content/Context.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestContext](AndroidTestCase.md))`(`context:` ` [Context](../android.content/Context.md)!`)` <br /> Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. Access to the latter is provided by the context set with the [setContext](AndroidTestCase.md))method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testAndroidTestCaseSetupProperly](AndroidTestCase.md))`()` <br /> | ||

| Inherited properties ||
|---|---|
| From class [AndroidTestCase](AndroidTestCase.md) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------| | [Context](../android.content/Context.md)! | [mContext](AndroidTestCase.md) <br /> | ||

## Public constructors

### ServiceTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServiceTestCase(serviceClass: Class<T>!)
```

Constructor

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------|
| `serviceClass` | [Class](../java.lang/Class.md)\<T\>!:The type of the service under test. |

## Public methods

### getApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApplication(): Application!
```

**Deprecated:** *Deprecated in Java.*

Returns the Application object in use by the service under test.

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------|
| [Application](../android.app/Application.md)! | The application object. |

**See Also**

- [#setApplication](ServiceTestCase.md)) 

### getService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getService(): T
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T | An instance of the service under test. This instance is created automatically when a test calls [startService](ServiceTestCase.md))or [bindService](ServiceTestCase.md)). |

### getSystemContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

Returns the real system context that is saved by [setUp()](ServiceTestCase.md)). Use it to create mock or other types of context objects for the service under test.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [Context](../android.content/Context.md)! | A normal system context. |

### setApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setApplication(application: Application!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the application that is used during the test. If you do not call this method, a new [MockApplication](../android.test.mock/MockApplication.md) object is used.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `application` | [Application](../android.app/Application.md)!:The Application object that is used by the service under test. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#getApplication()> 

### testServiceTestCaseSetUpProperly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun testServiceTestCaseSetUpProperly(): Unit
```

**Deprecated:** *Deprecated in Java.*

Tests that [setupService()](ServiceTestCase.md))runs correctly and issues an junit.framework.Assert#assertNotNull(String, Object) if it does. You can override this test method if you wish.

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |

## Protected methods

### bindService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun bindService(intent: Intent!): IBinder!
```

**Deprecated:** *Deprecated in Java.*

Starts the service under test, in the same way as if it were started by android.content.Context#bindService(Intent, ServiceConnection, int) with an [android.content.Intent](../android.content/Intent.md) that identifies a service.

Notice that the parameters are different. You do not provide a [android.content.ServiceConnection](../android.content/ServiceConnection.md) object or the flags parameter. Instead, you only provide the Intent. The method returns an object whose type is a subclass of [android.os.IBinder](../android.os/IBinder.md), or null if the method fails. An IBinder object refers to a communication channel between the application and the service. The flag is assumed to be [android.content.Context#BIND_AUTO_CREATE](../android.content/Context.md).

See [Designing a Remote Interface Using AIDL](https://developer.android.com/guide/components/aidl.html) for more information about the communication channel object returned by this method.
Note: To be able to use bindService in a test, the service must implement getService() method. An example of this is in the ApiDemos sample application, in the LocalService demo.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)!:An Intent object of the form expected by android.content.Context#bindService. |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [IBinder](../android.os/IBinder.md)! | An object whose type is a subclass of IBinder, for making further calls into the service. |

### setUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setUp(): Unit
```

**Deprecated:** *Deprecated in Java.*

Gets the current system context and stores it. Extend this method to do your own test initialization. If you do so, you must call`super.setUp()`as the first statement in your override. The method is called before each test method is executed. 

### setupService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setupService(): Unit
```

**Deprecated:** *Deprecated in Java.*

Creates the service under test and attaches all injected dependencies (Context, Application) to it. This is called automatically by [startService](ServiceTestCase.md))or by [bindService](ServiceTestCase.md)). If you need to call [setContext()](AndroidTestCase.md))or [setApplication()](ServiceTestCase.md)), do so before calling this method. 

### shutdownService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun shutdownService(): Unit
```

**Deprecated:** *Deprecated in Java.*

Makes the necessary calls to stop (or unbind) the service under test, and calls onDestroy(). Ordinarily this is called automatically (by [tearDown](ServiceTestCase.md)), but you can call it directly from your test in order to check for proper shutdown behavior. 

### startService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun startService(intent: Intent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts the service under test, in the same way as if it were started by [Context.startService(Intent)](../android.content/Context.md))with an [android.content.Intent](../android.content/Intent.md) that identifies a service. If you use this method to start the service, it is automatically stopped by [tearDown](ServiceTestCase.md)).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)!:An Intent that identifies a service, of the same form as the Intent passed to [Context.startService(Intent)](../android.content/Context.md)). |

### tearDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun tearDown(): Unit
```

**Deprecated:** *Deprecated in Java.*

Shuts down the service under test. Ensures all resources are cleaned up and garbage collected before moving on to the next test. This method is called after each test method.

Subclasses that override this method must call`super.tearDown()`as their last statement.

| Exceptions ||
|-----------------------|---|
| `java.lang.Exception` | |
