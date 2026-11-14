# ServiceTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceTestCase

Kotlin| [Java](https://developer.android.com/reference/android/test/ServiceTestCase "View this page in Java") 

```
abstract class ServiceTestCase<T : Service!> : AndroidTestCase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.test.AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase) ||
| | ↳ | [android.test.ServiceTestCase](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#) |

| **This class was deprecated in API level 24.**
|
| Use [ServiceTestRule](https://developer.android.com/reference/android/support/test/rule/ServiceTestRule.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This test case provides a framework in which you can test Service classes in a controlled environment. It provides basic support for the lifecycle of a Service, and hooks with which you can inject various dependencies and control the environment in which your Service is tested.
|
| ### Developer Guides
|
| For more information about application testing, read the [Testing](https://developer.android.com/guide/topics/testing/index.html) developer guide.

<br />

**Lifecycle Support.** A Service is accessed with a specific sequence of calls, as described in the [Services](http://developer.android.com/guide/topics/fundamentals/services.html) document. In order to support the lifecycle of a Service,`ServiceTestCase`enforces this protocol:

- The [setUp()](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setUp())method is called before each test method. The base implementation gets the system context. If you override`setUp()`, you must call`super.setUp()`as the first statement in your override.
- The test case waits to call [android.app.Service#onCreate()](https://developer.android.com/reference/kotlin/android/app/Service.html#onCreate())until one of your test methods calls [startService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#startService(android.content.Intent))or [bindService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#bindService(android.content.Intent)). This gives you an opportunity to set up or adjust any additional framework or test logic before you test the running service.
- When one of your test methods calls [ServiceTestCase.startService()](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#startService(android.content.Intent))or [ServiceTestCase.bindService()](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#bindService(android.content.Intent)), the test case calls [Service.onCreate()](https://developer.android.com/reference/kotlin/android/app/Service.html#onCreate())and then calls either [Service.startService(Intent)](https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#startService(android.content.Intent))or android.app.Service#bindService(Intent, ServiceConnection, int), as appropriate. It also stores values needed to track and support the lifecycle.
- After each test method finishes, the test case calls the [tearDown](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#tearDown())method. This method stops and destroys the service with the appropriate calls, depending on how the service was started. If you override`tearDown()`, your must call the`super.tearDown()`as the last statement in your override.

**Dependency Injection.** A service has two inherent dependencies, its [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) and its associated [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#). The ServiceTestCase framework allows you to inject modified, mock, or isolated replacements for these dependencies, and thus perform unit tests with controlled dependencies in an isolated environment.

By default, the test case is injected with a full system context and a generic [MockApplication](https://developer.android.com/reference/kotlin/android/test/mock/MockApplication) object. You can inject alternatives to either of these by invoking [setContext()](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context))or [setApplication()](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setApplication(android.app.Application)). You must do this*before* calling startService() or bindService(). The test framework provides a number of alternatives for Context, including [MockContext](https://developer.android.com/reference/kotlin/android/test/mock/MockContext), [RenamingDelegatingContext](https://developer.android.com/reference/kotlin/android/test/RenamingDelegatingContext), [ContextWrapper](https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#), and [android.test.IsolatedContext](https://developer.android.com/reference/kotlin/android/test/IsolatedContext).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServiceTestCase](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#ServiceTestCase(java.lang.Class))`(`serviceClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` Constructor |

| Public methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)! | [getApplication](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#getApplication())`()` Returns the Application object in use by the service under test. |
| openT | [getService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#getService())`()` <br /> |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getSystemContext](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#getSystemContext())`()` Returns the real system context that is saved by [setUp()](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setUp()). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setApplication](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setApplication(android.app.Application))`(`application:` ` [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)!`)` Sets the application that is used during the test. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testServiceTestCaseSetUpProperly](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#testServiceTestCaseSetUpProperly())`()` Tests that [setupService()](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setupService())runs correctly and issues an junit. |

| Protected methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)! | [bindService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#bindService(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Starts the service under test, in the same way as if it were started by android. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUp](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setUp())`()` Gets the current system context and stores it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setupService())`()` Creates the service under test and attaches all injected dependencies (Context, Application) to it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdownService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#shutdownService())`()` Makes the necessary calls to stop (or unbind) the service under test, and calls onDestroy(). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#startService(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Starts the service under test, in the same way as if it were started by [Context.startService(Intent)](https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent))with an [android.content.Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) that identifies a service. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tearDown](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#tearDown())`()` Shuts down the service under test. |

| Inherited functions ||
|---|---|
| From class [AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertActivityRequiresPermission](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertActivityRequiresPermission(kotlin.String,%20kotlin.String,%20kotlin.String))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `className:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that launching a given activity is protected by a particular permission by attempting to start the activity and validating that a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown that mentions the permission in its error message. Note that an instrumentation isn't needed because all we are looking for is a security error and we don't need to wait for the activity to launch and get a handle to the activity. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertReadingContentUriRequiresPermission](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertReadingContentUriRequiresPermission(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that reading from the content uri requires a particular permission by querying the uri and ensuring a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown mentioning the particular permission. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertWritingContentUriRequiresPermission](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#assertWritingContentUriRequiresPermission(android.net.Uri,%20kotlin.String))`(`uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`, `permission:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Asserts that writing to the content uri requires a particular permission by inserting into the uri and ensuring a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) is thrown mentioning the particular permission. <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getContext())`()` <br /> | | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getTestContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#getTestContext())`()` <br /> Returns the test context that was set via [setTestContext(android.content.Context)](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrubClass](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#scrubClass(java.lang.Class))`(`testCaseClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` <br /> This function is called by various TestCase implementations, at tearDown() time, in order to scrub out any class variables. This protects against memory leaks in the case where a test case creates a non-static inner class (thus referencing the test case) and gives it to someone else to hold onto. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setTestContext(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> Test context can be used to access resources from the test's own package as opposed to the resources from the test target package. Access to the latter is provided by the context set with the [setContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context))method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testAndroidTestCaseSetupProperly](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#testAndroidTestCaseSetupProperly())`()` <br /> | ||

| Inherited properties ||
|---|---|
| From class [AndroidTestCase](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase) |------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------| | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [mContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#mContext:android.content.Context) <br /> | ||

## Public constructors

### ServiceTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ServiceTestCase(serviceClass: Class<T>!)
```

Constructor

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------|
| `serviceClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:The type of the service under test. |

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
| [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)! | The application object. |

**See Also**

- [#setApplication](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setApplication(android.app.Application)) 

### getService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getService(): T
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T | An instance of the service under test. This instance is created automatically when a test calls [startService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#startService(android.content.Intent))or [bindService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#bindService(android.content.Intent)). |

### getSystemContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

Returns the real system context that is saved by [setUp()](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setUp()). Use it to create mock or other types of context objects for the service under test.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | A normal system context. |

### setApplication

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setApplication(application: Application!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the application that is used during the test. If you do not call this method, a new [MockApplication](https://developer.android.com/reference/kotlin/android/test/mock/MockApplication) object is used.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `application` | [Application](https://developer.android.com/reference/kotlin/android/app/Application.html#)!:The Application object that is used by the service under test. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#getApplication()> 

### testServiceTestCaseSetUpProperly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun testServiceTestCaseSetUpProperly(): Unit
```

**Deprecated:** *Deprecated in Java.*

Tests that [setupService()](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setupService())runs correctly and issues an junit.framework.Assert#assertNotNull(String, Object) if it does. You can override this test method if you wish.

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

Starts the service under test, in the same way as if it were started by android.content.Context#bindService(Intent, ServiceConnection, int) with an [android.content.Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) that identifies a service.

Notice that the parameters are different. You do not provide a [android.content.ServiceConnection](https://developer.android.com/reference/kotlin/android/content/ServiceConnection.html#) object or the flags parameter. Instead, you only provide the Intent. The method returns an object whose type is a subclass of [android.os.IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#), or null if the method fails. An IBinder object refers to a communication channel between the application and the service. The flag is assumed to be [android.content.Context#BIND_AUTO_CREATE](https://developer.android.com/reference/kotlin/android/content/Context.html#BIND_AUTO_CREATE:kotlin.Int).

See [Designing a Remote Interface Using AIDL](https://developer.android.com/guide/components/aidl.html) for more information about the communication channel object returned by this method.
Note: To be able to use bindService in a test, the service must implement getService() method. An example of this is in the ApiDemos sample application, in the LocalService demo.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:An Intent object of the form expected by android.content.Context#bindService. |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)! | An object whose type is a subclass of IBinder, for making further calls into the service. |

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

Creates the service under test and attaches all injected dependencies (Context, Application) to it. This is called automatically by [startService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#startService(android.content.Intent))or by [bindService](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#bindService(android.content.Intent)). If you need to call [setContext()](https://developer.android.com/reference/kotlin/android/test/AndroidTestCase#setContext(android.content.Context))or [setApplication()](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#setApplication(android.app.Application)), do so before calling this method. 

### shutdownService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun shutdownService(): Unit
```

**Deprecated:** *Deprecated in Java.*

Makes the necessary calls to stop (or unbind) the service under test, and calls onDestroy(). Ordinarily this is called automatically (by [tearDown](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#tearDown()), but you can call it directly from your test in order to check for proper shutdown behavior. 

### startService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun startService(intent: Intent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts the service under test, in the same way as if it were started by [Context.startService(Intent)](https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent))with an [android.content.Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) that identifies a service. If you use this method to start the service, it is automatically stopped by [tearDown](https://developer.android.com/reference/kotlin/android/test/ServiceTestCase#tearDown()).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:An Intent that identifies a service, of the same form as the Intent passed to [Context.startService(Intent)](https://developer.android.com/reference/kotlin/android/content/Context.html#startService(android.content.Intent)). |

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
