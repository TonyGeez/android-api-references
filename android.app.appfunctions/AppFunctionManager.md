Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionManager

```
class AppFunctionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appfunctions.AppFunctionManager](AppFunctionManager.md) |

Provides access to App Functions.

See `https://developer.android.com/reference/kotlin/android/app/appfunctions/package-summary` for a comprehensive overview of App Functions.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#APP_FUNCTION_STATE_DEFAULT:kotlin.Int` The default state of the app function. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#APP_FUNCTION_STATE_DISABLED:kotlin.Int` The app function is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#APP_FUNCTION_STATE_ENABLED:kotlin.Int` The app function is enabled. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#PROPERTY_SUPPORT_APP_FUNCTION_USER_CONTROL:kotlin.String` Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag that informs the system whether the app supports runtime user control when invoking app functions. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | executeAppFunction Executes the app function. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | executeAppFunction Executes the app function with an `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.html#`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getAppFunctionActivityStates Retrieves the registered app functions for the specified activities. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getAppFunctionStates Retrieves the runtime state of the specified app functions. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | isAppFunctionEnabled Retrieves whether an app function is enabled (allows execution). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | isAppFunctionEnabled Retrieves whether an app function owned by the calling package is enabled (allows execution). |
| --- | --- |
| [AppFunctionObservation](AppFunctionObservation.md) | observeAppFunctions Registers an observer to monitor changes to app functions within packages that the caller can query. |
| [AppFunctionRegistration](AppFunctionRegistration.md) | registerAppFunction Registers a runtime implementation for an app function, that can be executed using #executeAppFunction. |
| [AppFunctionRegistration](AppFunctionRegistration.md) | registerAppFunctions Registers several AppFunction implementations at once, sharing a single lifecycle. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | searchAppFunctions Searches app function AppFunctionMetadatas. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAppFunctionEnabled Sets the enabled state of the app function owned by the calling package. |

## Constants

### APP_FUNCTION_STATE_DEFAULT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_FUNCTION_STATE_DEFAULT: Int
```

The default state of the app function.

To reset the enabled state to the default value, call setAppFunctionEnabled with this value.

 Value: 0

### APP_FUNCTION_STATE_DISABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_FUNCTION_STATE_DISABLED: Int
```

The app function is disabled.

To disable an app function, call setAppFunctionEnabled with this value.

 Value: 2

### APP_FUNCTION_STATE_ENABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_FUNCTION_STATE_ENABLED: Int
```

The app function is enabled.

To enable an app function, call setAppFunctionEnabled with this value.

 Value: 1

### PROPERTY_SUPPORT_APP_FUNCTION_USER_CONTROL

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SUPPORT_APP_FUNCTION_USER_CONTROL: String
```

Application level `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.Property.html#` tag that informs the system whether the app supports runtime user control when invoking app functions.

Setting this property to `true` indicates that the app supports runtime user control. Therefore, the system will no longer automatically grant "always allow" access to the caller at package installation time.

Setting this property to `false` (or leaving it unset) indicates that the app has not migrated to runtime user control. To maintain compatibility, the system will grant the caller "always allow" access by default. However, users can still manually adjust the permission in system settings to restrict or block this access.

This property will stop being respected in a future Android release.

**Syntax:**

```kotlin
<application>
    <property
      android:name="android.app.appfunctions.PROPERTY_SUPPORTS_APP_FUNCTION_USER_CONTROL"
      android:value="true|false"/>
  </application>
  
```

 Value: "android.app.appfunctions.PROPERTY_SUPPORTS_APP_FUNCTION_USER_CONTROL"

## Public methods

### executeAppFunction

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun executeAppFunction(
    request: ExecuteAppFunctionRequest, 
    executor: Executor, 
    cancellationSignal: CancellationSignal, 
    callback: OutcomeReceiver<ExecuteAppFunctionResponse!, AppFunctionException!>
): Unit
```

Executes the app function.

Applications can execute functions they define. To execute functions defined in another component, the caller must have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#EXECUTE_APP_FUNCTIONS:kotlin.String` or `android.permission.EXECUTE_APP_FUNCTIONS_SYSTEM` permissions.

A function can only be executed while its isEnabled is true.

See AppFunctionException for possible failures.

| Parameters ||
|---|---|
| `request` | [ExecuteAppFunctionRequest](ExecuteAppFunctionRequest.md): the request to execute the app function. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor to run the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md): the cancellation signal to cancel the execution. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [ExecuteAppFunctionResponse](ExecuteAppFunctionResponse.md)!, [AppFunctionException](AppFunctionException.md)!\>: the callback to receive the function execution result or error. This value cannot be `null`. |

### executeAppFunction

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun executeAppFunction(
    appInteractionSession: AppInteractionSession, 
    request: ExecuteAppFunctionRequest, 
    executor: Executor, 
    cancellationSignal: CancellationSignal, 
    callback: OutcomeReceiver<ExecuteAppFunctionResponse!, AppFunctionException!>
): Unit
```

Executes the app function with an `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.html#`.

Applications can execute functions they define. To execute functions defined in another component, the caller must have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#EXECUTE_APP_FUNCTIONS:kotlin.String` or `android.permission.EXECUTE_APP_FUNCTIONS_SYSTEM` permissions.

A function can only be executed while its isEnabled is true.

See AppFunctionException for possible failures.

| Parameters ||
|---|---|
| `appInteractionSession` | [AppInteractionSession](../android.app/AppInteractionSession.md): the app interaction session to associate with the function execution. This value cannot be `null`. |
| `request` | [ExecuteAppFunctionRequest](ExecuteAppFunctionRequest.md): the request to execute the app function. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor to run the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md): the cancellation signal to cancel the execution. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [ExecuteAppFunctionResponse](ExecuteAppFunctionResponse.md)!, [AppFunctionException](AppFunctionException.md)!\>: the callback to receive the function execution result or error. This value cannot be `null`. |

**See Also**

- createSession

### getAppFunctionActivityStates

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAppFunctionActivityStates(
    activityIds: MutableSet<AppFunctionActivityId!>, 
    executor: Executor, 
    callback: OutcomeReceiver<MutableList<AppFunctionActivityState!>!, Exception!>
): Unit
```

Retrieves the registered app functions for the specified activities.

Each AppFunctionActivityState contains the set of registered AppFunctionNames associated with a requested AppFunctionActivityId.

Functions that do not exist or are not visible to the calling application will be silently omitted from the result. Requested activities that have no registered functions will be omitted from the result.

See AppFunctionActivityId for potential usages, including conversion from `https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ActivityId.html#`.

This method follows the same permission rules as searchAppFunctions.

See getAppFunctionStates for retrieving the runtime state of app functions based on their names.

See searchAppFunctions on how to retrieve the AppFunctionMetadata of app functions.

See observeAppFunctions for observing changes to app functions' AppFunctionMetadata and AppFunctionStates.

| Parameters ||
|---|---|
| `activityIds` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppFunctionActivityId](../android/app/appfunctions/AppFunctionActivityId.md)!\>: The set of activity IDs to retrieve function states for. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor to run the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppFunctionActivityState](AppFunctionActivityState.md)!\>!, [Exception](../java.lang/Exception.md)!\>: The callback to receive the list of activity states. This value cannot be `null`. |
| --- | --- |

**See Also**

- getAppFunctionActivityId

### getAppFunctionStates

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAppFunctionStates(
    appFunctionNames: MutableList<AppFunctionName!>, 
    executor: Executor, 
    callback: OutcomeReceiver<MutableList<AppFunctionState!>!, Exception!>
): Unit
```

Retrieves the runtime state of the specified app functions.

This includes runtime-changing properties such as whether the functions are currently enabled or disabled. Functions that do not exist or are not visible to the calling application will be silently omitted from the result list.

This method follows the same permission rules as searchAppFunctions.

See getAppFunctionActivityStates for retrieving the states of app functions associated with a specific activity.

See searchAppFunctions on how to retrieve the AppFunctionMetadata of app functions.

See observeAppFunctions for observing changes to app functions' AppFunctionMetadata and AppFunctionStates.

| Parameters ||
|---|---|
| `appFunctionNames` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppFunctionName](../android/app/appfunctions/AppFunctionName.md)!\>: The names of the app functions to request the state for. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor to run the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppFunctionState](../android/app/appfunctions/AppFunctionState.md)!\>!, [Exception](../java.lang/Exception.md)!\>: The callback to receive the function state result. This value cannot be `null`. |
| --- | --- |

### isAppFunctionEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAppFunctionEnabled(
    functionIdentifier: String, 
    targetPackage: String, 
    executor: Executor, 
    callback: OutcomeReceiver<Boolean!, Exception!>
): Unit
```

Retrieves whether an app function is enabled (allows execution).

This is equivalent to calling getAppFunctionStates and checking the isEnabled property of the result. Consider using getAppFunctionStates to get the full state of the app function.

If the operation fails, the callback's onError is called with errors:

- `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`, if the function is not found or the caller does not have access to it.

| Parameters ||
|---|---|
| `functionIdentifier` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the identifier of the app function to check (unique within the target package). This value cannot be `null`. |
| `targetPackage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the package name of the app function's owner. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor to run the request. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!, [Exception](../java.lang/Exception.md)!\>: the callback to receive the function enabled check result. This value cannot be `null`. |

**See Also**

- isEnabled

### isAppFunctionEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAppFunctionEnabled(
    functionIdentifier: String, 
    executor: Executor, 
    callback: OutcomeReceiver<Boolean!, Exception!>
): Unit
```

Retrieves whether an app function owned by the calling package is enabled (allows execution).

Same as isAppFunctionEnabled but only for checking functions owned by the calling package.

This is equivalent to calling getAppFunctionStates and checking the isEnabled property of the result. Consider using getAppFunctionStates to get the full state of the app function.

| Parameters ||
|---|---|
| `functionIdentifier` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the identifier of the app function to check (unique within the target package). This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor to run the request. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!, [Exception](../java.lang/Exception.md)!\>: the callback to receive the function enabled check result. This value cannot be `null`. |
| --- | --- |

### observeAppFunctions

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun observeAppFunctions(
    executor: Executor, 
    appFunctionObserver: AppFunctionObserver
): AppFunctionObservation
```

Registers an observer to monitor changes to app functions within packages that the caller can query.

The caller should retain a reference to the returned AppFunctionObservation, and call cancel when observation is no longer required.

The callback is only triggered by changes after its registration. Any changes that occur before the registration are not reported.

An example usage flow is:

1. Call observeAppFunctions, to start monitoring app function changes, using the AppFunctionObserver.
2. Call searchAppFunctions and getAppFunctionStates to get the initial list of app functions and their states.
3. In onAppFunctionMetadataChanged, call searchAppFunctions with a AppFunctionSearchSpec that matches the changed packages to get the updated metadata.
4. In onAppFunctionStatesChanged, call getAppFunctionStates with the list of AppFunctionNames that matches the changed functions to get the updated states.

 Note that this is guaranteed to trigger after onAppFunctionMetadataChanged for new functions or functions that also changed states, so there's no need to call getAppFunctionStates in onAppFunctionMetadataChanged.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor to run the AppFunctionObserver callbacks. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `appFunctionObserver` | [AppFunctionObserver](AppFunctionObserver.md): the observer to receive updates to registered app functions. This value cannot be `null`. |

| Return ||
|---|---|
| AppFunctionObservation | An AppFunctionObservation used to cancel this observation. This value cannot be `null`. |

### registerAppFunction

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerAppFunction(
    functionIdentifier: String, 
    executor: Executor, 
    appFunction: AppFunction
): AppFunctionRegistration
```

Registers a runtime implementation for an app function, that can be executed using #executeAppFunction.

executeAppFunction targeting an app function provided by this method will trigger the onExecuteAppFunction method of the provided implementation, as long as the process registering it is not frozen, and the `https://developer.android.com/reference/kotlin/android/content/Context.html#` registering it is not destroyed (at which point the registration will be removed).

You must declare the app function in your `AndroidManifest.xml` using an application-level `<property>` named `android.app.appfunctions`. See AppFunctionMetadata for details on the XML schema (`your_app_functions.xml` in the example below).

**Example manifest declaration:**

```kotlin
<code>&lt;application ...&gt;
    &lt;property
        android:name="android.app.appfunctions"
        android:value="your_app_functions.xml" /&gt;
    ...
  &lt;/application&gt;
  </code>
```

Function implementations can only be registered from `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or `https://developer.android.com/reference/kotlin/android/app/Service.html#` contexts. If registering from an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, strongly consider `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int` for your function definition.

The `functionIdentifier` must correspond to an app function declared in your app's application-level XML assets. If the identifier is not found, this method will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. Attempting to register a duplicate function based on the rules of getScope will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

To register multiple functions at once, consider using registerAppFunctions as a more efficient alternative.

The system holds a strong reference to the provided AppFunction implementation as long as it is registered. To prevent memory leaks and ensure the system is aware that the function is no longer available, you must explicitly call unregister when the function is no longer relevant (e.g., in onStop or before android.app.Service#stopForeground).

| Parameters ||
|---|---|
| `functionIdentifier` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The unique identifier for the function, which must match an entry in the app's XML resource declarations. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which the function will be invoked. This value cannot be `null`. |
| `appFunction` | [AppFunction](AppFunction.md): The AppFunction implementation to be executed when the function is triggered. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| AppFunctionRegistration | A AppFunctionRegistration object that can be used to unregister the function. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the provided `functionIdentifier` is not declared in the app's application-level XML resources or if an activity-scoped function is registered from a non-Activity context. |
| `java.lang.IllegalStateException` | if a duplicate function is already registered (see getScope), or if not called from `https://developer.android.com/reference/kotlin/android/app/Activity.html#` or `https://developer.android.com/reference/kotlin/android/app/Service.html#` contexts. |

### registerAppFunctions

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerAppFunctions(requests: MutableList<RegisterAppFunctionRequest!>): AppFunctionRegistration
```

Registers several AppFunction implementations at once, sharing a single lifecycle.

This is a more efficient alternative to calling registerAppFunction multiple times.

### Behavior and Lifecycle

Each function registered through this method follows the same execution and lifecycle rules as those registered with registerAppFunction.

### Batch Operation and Atomicity

The registration is atomic: either all functions in the provided list are registered successfully, or none are. If any function in the list fails validation (e.g., its is already registered or not declared in the manifest), this method will throw an exception, and no functions from the batch will be registered. Each function in the request follows the scoping rules declared in the app's XML resources.

A single AppFunctionRegistration object is returned, which can be used to unregister the entire batch of functions with one call.

| Parameters ||
|---|---|
| `requests` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RegisterAppFunctionRequest](../android/app/appfunctions/RegisterAppFunctionRequest.md)!\>: A list of RegisterAppFunctionRequest objects, each specifying a function to be registered. This value cannot be `null`. |

| Return ||
|---|---|
| AppFunctionRegistration | A single AppFunctionRegistration object that can be used to unregister all the functions in the batch with one call. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any getFunctionIdentifier is not declared in the app's application-level XML assets or the `requests` list is empty. |
| `java.lang.IllegalStateException` | if any function in the `requests` list is already registered by this app. |

### searchAppFunctions

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun searchAppFunctions(
    searchSpec: AppFunctionSearchSpec, 
    executor: Executor, 
    callback: OutcomeReceiver<MutableList<AppFunctionMetadata!>!, Exception!>
): Unit
```

Searches app function AppFunctionMetadatas.

Note that the state is not guaranteed to be the latest, as metadata can change between request and execute times when apps are updated.

The calling app can search for:

- Functions in its own package (no permission required).
- Functions in other packages that it is allowed to query via android.content.pm.PackageManager#canPackageQuery when holding the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#EXECUTE_APP_FUNCTIONS:kotlin.String` permission.
- Functions in other packages that it is allowed to query via android.content.pm.PackageManager#canPackageQuery when holding either the `android.permission.EXECUTE_APP_FUNCTIONS_SYSTEM` or `android.permission.DISCOVER_APP_FUNCTIONS` permission on API level 37 and above.

See getAppFunctionStates and getAppFunctionActivityStates on how to retrieve the runtime state of app functions.

See observeAppFunctions for observing changes to app functions' AppFunctionMetadata and AppFunctionStates.

| Parameters ||
|---|---|
| `searchSpec` | [AppFunctionSearchSpec](AppFunctionSearchSpec.md): The spec of app functions to search for. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor to run the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppFunctionMetadata](AppFunctionMetadata.md)!\>!, [Exception](../java.lang/Exception.md)!\>: The callback to receive the search results. This value cannot be `null`. |
| --- | --- |

### setAppFunctionEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAppFunctionEnabled(
    functionIdentifier: String, 
    newEnabledState: Int, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, Exception!>
): Unit
```

Sets the enabled state of the app function owned by the calling package.

**Important:** This method only applies to functions backed by an AppFunctionService. It cannot be used to modify the state of functions registered at runtime. For runtime-registered app functions, use registerAppFunction to register them and unregister to unregister them instead.

| Parameters ||
|---|---|
| `functionIdentifier` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the identifier of the app function to enable (unique within the calling package). This value cannot be `null`. |
| `newEnabledState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new state of the app function. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#APP_FUNCTION_STATE_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#APP_FUNCTION_STATE_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#APP_FUNCTION_STATE_DISABLED:kotlin.Int` |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor to run the callback. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [Exception](../java.lang/Exception.md)!\>: the callback to receive the result of the function enablement. Can return `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if the function is not found or the caller does not have access to it. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the function is runtime-registered. |
