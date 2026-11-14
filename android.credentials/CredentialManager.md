Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CredentialManager

```
class CredentialManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.credentials.CredentialManager](CredentialManager.md) |

Manages user authentication flows.

Note that an application should call the Jetpack CredentialManager apis instead of directly calling these framework apis.

The CredentialManager apis launch framework UI flows for a user to register a new credential or to consent to a saved credential from supported credential providers, which can then be used to authenticate to the app. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CREDENTIALS:kotlin.String` feature which can be detected using hasSystemFeature.

## Summary

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clearCredentialState Clears the current user credential state from all credential providers. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | createCredential Launches the necessary flows to register an app credential for the user. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getCredential Launches the necessary flows to retrieve an app credential from the user. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getCredential Launches the remaining flows to retrieve an app credential from the user, after the completed prefetch work corresponding to the given `pendingGetCredentialHandle`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEnabledCredentialProviderService Returns `true` if the calling application provides a CredentialProviderService that is enabled for the current user, or `false` otherwise. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | prepareGetCredential Prepare for a get-credential operation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerCredentialDescription Registers a CredentialDescription for an actively provisioned Credential a CredentialProvider has. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterCredentialDescription Unregisters a CredentialDescription for an actively provisioned Credential that has been registered previously. |

## Public methods

### clearCredentialState

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearCredentialState(
    request: ClearCredentialStateRequest, 
    cancellationSignal: CancellationSignal?, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, ClearCredentialStateException!>
): Unit
```

Clears the current user credential state from all credential providers.

You should invoked this api after your user signs out of your app to notify all credential providers that any stored credential session for the given app should be cleared.

A credential provider may have stored an active credential session and use it to limit sign-in options for future get-credential calls. For example, it may prioritize the active credential over any other available credential. When your user explicitly signs out of your app and in order to get the holistic sign-in options the next time, you should call this API to let the provider clear any stored credential session.

| Parameters ||
|---|---|
| `request` | [ClearCredentialStateRequest](ClearCredentialStateRequest.md): the request data. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [ClearCredentialStateException](ClearCredentialStateException.md)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

### createCredential

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createCredential(
    context: Context, 
    request: CreateCredentialRequest, 
    cancellationSignal: CancellationSignal?, 
    executor: Executor, 
    callback: OutcomeReceiver<CreateCredentialResponse!, CreateCredentialException!>
): Unit
```

Launches the necessary flows to register an app credential for the user.

The execution can potentially launch UI flows to collect user consent to creating or storing the new credential, etc. Callers (e.g. browsers) may optionally set origin in CreateCredentialRequest for an app different from their own, to be able to get credentials on behalf of that app. They would need additional permission `CREDENTIAL_MANAGER_SET_ORIGIN` to use this functionality

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): the context used to launch any UI needed; use an activity context to make sure the UI will be launched within the same task stack. This value cannot be `null`. |
| `request` | [CreateCredentialRequest](CreateCredentialRequest.md): the request specifying type(s) of credentials to get from the user. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [CreateCredentialResponse](CreateCredentialResponse.md)!, [CreateCredentialException](CreateCredentialException.md)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

### getCredential

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCredential(
    context: Context, 
    request: GetCredentialRequest, 
    cancellationSignal: CancellationSignal?, 
    executor: Executor, 
    callback: OutcomeReceiver<GetCredentialResponse!, GetCredentialException!>
): Unit
```

Launches the necessary flows to retrieve an app credential from the user.

The execution can potentially launch UI flows to collect user consent to using a credential, display a picker when multiple credentials exist, etc. Callers (e.g. browsers) may optionally set origin in GetCredentialRequest for an app different from their own, to be able to get credentials on behalf of that app. They would need additional permission `CREDENTIAL_MANAGER_SET_ORIGIN` to use this functionality

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): the context used to launch any UI needed; use an activity context to make sure the UI will be launched within the same task stack. This value cannot be `null`. |
| `request` | [GetCredentialRequest](GetCredentialRequest.md): the request specifying type(s) of credentials to get from the user. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [GetCredentialResponse](GetCredentialResponse.md)!, [GetCredentialException](GetCredentialException.md)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

### getCredential

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCredential(
    context: Context, 
    pendingGetCredentialHandle: PrepareGetCredentialResponse.PendingGetCredentialHandle, 
    cancellationSignal: CancellationSignal?, 
    executor: Executor, 
    callback: OutcomeReceiver<GetCredentialResponse!, GetCredentialException!>
): Unit
```

Launches the remaining flows to retrieve an app credential from the user, after the completed prefetch work corresponding to the given `pendingGetCredentialHandle`.

The execution can potentially launch UI flows to collect user consent to using a credential, display a picker when multiple credentials exist, etc.

Use this API to complete the full credential retrieval operation after you initiated a request through the prepareGetCredential API.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): the context used to launch any UI needed; use an activity context to make sure the UI will be launched within the same task stack. This value cannot be `null`. |
| `pendingGetCredentialHandle` | [PrepareGetCredentialResponse.PendingGetCredentialHandle](../android/credentials/PrepareGetCredentialResponse.PendingGetCredentialHandle.md): the handle representing the pending operation to resume. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [GetCredentialResponse](GetCredentialResponse.md)!, [GetCredentialException](GetCredentialException.md)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

### isEnabledCredentialProviderService

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEnabledCredentialProviderService(componentName: ComponentName): Boolean
```

Returns `true` if the calling application provides a CredentialProviderService that is enabled for the current user, or `false` otherwise. CredentialProviderServices are enabled on a per-service basis so the individual component name of the service should be passed in here. **Usage of this API is encouraged in API level 35 and above. It may throw a NullPointerException on certain devices running other API versions.**

| Parameters ||
|---|---|
| `componentName` | [ComponentName](../android.content/ComponentName.md): the component name to check is enabled. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the componentName package does not match the calling package name this call will throw an exception |
| `java.lang.NullPointerException` | Usage of this API is discouraged as it is not fully functional, and may throw a NullPointerException on certain devices and/or API versions |

### prepareGetCredential

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun prepareGetCredential(
    request: GetCredentialRequest, 
    cancellationSignal: CancellationSignal?, 
    executor: Executor, 
    callback: OutcomeReceiver<PrepareGetCredentialResponse!, GetCredentialException!>
): Unit
```

Prepare for a get-credential operation. Returns a PrepareGetCredentialResponse that can launch the credential retrieval UI flow to request a user credential for your app.

This API doesn't invoke any UI. It only performs the preparation work so that you can later launch the remaining get-credential operation (involves UIs) through the getCredential API which incurs less latency compared to the getCredential API that executes the whole operation in one call.

| Parameters ||
|---|---|
| `request` | [GetCredentialRequest](GetCredentialRequest.md): the request specifying type(s) of credentials to get from the user. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [PrepareGetCredentialResponse](PrepareGetCredentialResponse.md)!, [GetCredentialException](GetCredentialException.md)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

### registerCredentialDescription

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerCredentialDescription(request: RegisterCredentialDescriptionRequest): Unit
```

Registers a CredentialDescription for an actively provisioned Credential a CredentialProvider has. This registry will then be used to determine where to fetch the requested Credential from. Not all credential types will be supported. The distinction will be made by the JetPack layer. For the types that are supported, JetPack will add a new key-value pair into GetCredentialRequest. These will not be persistent on the device. The Credential Providers will need to call this API again upon device reboot.

| Parameters ||
|---|---|
| `request` | [RegisterCredentialDescriptionRequest](RegisterCredentialDescriptionRequest.md): the request data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the calling Credential Provider can not handle one or more of the Credential Types that are sent for registration. |
| `java.lang.UnsupportedOperationException` | if the feature has not been enabled. |

### unregisterCredentialDescription

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterCredentialDescription(request: UnregisterCredentialDescriptionRequest): Unit
```

Unregisters a CredentialDescription for an actively provisioned Credential that has been registered previously.

| Parameters ||
|---|---|
| `request` | [UnregisterCredentialDescriptionRequest](UnregisterCredentialDescriptionRequest.md): the request data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the feature has not been enabled. |
