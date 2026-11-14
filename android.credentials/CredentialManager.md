Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CredentialManager

```
class CredentialManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.credentials.CredentialManager](https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#) |

Manages user authentication flows.

Note that an application should call the Jetpack CredentialManager apis instead of directly calling these framework apis.

The CredentialManager apis launch framework UI flows for a user to register a new credential or to consent to a saved credential from supported credential providers, which can then be used to authenticate to the app. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_CREDENTIALS:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

## Summary

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#clearCredentialState(android.credentials.ClearCredentialStateRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateRequest, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException!>)` Clears the current user credential state from all credential providers. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#createCredential(android.content.Context,%20android.credentials.CreateCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, request: https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialResponse!, https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialException!>)` Launches the necessary flows to register an app credential for the user. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, request: https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse!, https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException!>)` Launches the necessary flows to retrieve an app credential from the user. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.PrepareGetCredentialResponse.PendingGetCredentialHandle,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, pendingGetCredentialHandle: https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse.PendingGetCredentialHandle, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse!, https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException!>)` Launches the remaining flows to retrieve an app credential from the user, after the completed prefetch work corresponding to the given `pendingGetCredentialHandle`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#isEnabledCredentialProviderService(android.content.ComponentName)(componentName: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)` Returns `true` if the calling application provides a CredentialProviderService that is enabled for the current user, or `false` otherwise. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#prepareGetCredential(android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest, cancellationSignal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse!, https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException!>)` Prepare for a get-credential operation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#registerCredentialDescription(android.credentials.RegisterCredentialDescriptionRequest)(request: https://developer.android.com/reference/kotlin/android/credentials/RegisterCredentialDescriptionRequest)` Registers a `https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription` for an actively provisioned `https://developer.android.com/reference/kotlin/android/credentials/Credential` a CredentialProvider has. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#unregisterCredentialDescription(android.credentials.UnregisterCredentialDescriptionRequest)(request: https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest)` Unregisters a `https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription` for an actively provisioned `https://developer.android.com/reference/kotlin/android/credentials/Credential` that has been registered previously. |

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
| `request` | [ClearCredentialStateRequest](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateRequest): the request data. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

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

The execution can potentially launch UI flows to collect user consent to creating or storing the new credential, etc. Callers (e.g. browsers) may optionally set origin in `https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest` for an app different from their own, to be able to get credentials on behalf of that app. They would need additional permission `CREDENTIAL_MANAGER_SET_ORIGIN` to use this functionality

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the context used to launch any UI needed; use an activity context to make sure the UI will be launched within the same task stack. This value cannot be `null`. |
| `request` | [CreateCredentialRequest](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest): the request specifying type(s) of credentials to get from the user. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [CreateCredentialResponse](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialResponse)!, [CreateCredentialException](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialException)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

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

The execution can potentially launch UI flows to collect user consent to using a credential, display a picker when multiple credentials exist, etc. Callers (e.g. browsers) may optionally set origin in `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest` for an app different from their own, to be able to get credentials on behalf of that app. They would need additional permission `CREDENTIAL_MANAGER_SET_ORIGIN` to use this functionality

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the context used to launch any UI needed; use an activity context to make sure the UI will be launched within the same task stack. This value cannot be `null`. |
| `request` | [GetCredentialRequest](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest): the request specifying type(s) of credentials to get from the user. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [GetCredentialResponse](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse)!, [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

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

Use this API to complete the full credential retrieval operation after you initiated a request through the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#prepareGetCredential(android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` API.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): the context used to launch any UI needed; use an activity context to make sure the UI will be launched within the same task stack. This value cannot be `null`. |
| `pendingGetCredentialHandle` | [PrepareGetCredentialResponse.PendingGetCredentialHandle](https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse.PendingGetCredentialHandle): the handle representing the pending operation to resume. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| --- | --- |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [GetCredentialResponse](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse)!, [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

### isEnabledCredentialProviderService

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEnabledCredentialProviderService(componentName: ComponentName): Boolean
```

Returns `true` if the calling application provides a CredentialProviderService that is enabled for the current user, or `false` otherwise. CredentialProviderServices are enabled on a per-service basis so the individual component name of the service should be passed in here. **Usage of this API is encouraged in API level 35 and above. It may throw a NullPointerException on certain devices running other API versions.**

| Parameters ||
|---|---|
| `componentName` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): the component name to check is enabled. This value cannot be `null`. |

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

Prepare for a get-credential operation. Returns a `https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse` that can launch the credential retrieval UI flow to request a user credential for your app.

This API doesn't invoke any UI. It only performs the preparation work so that you can later launch the remaining get-credential operation (involves UIs) through the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.PrepareGetCredentialResponse.PendingGetCredentialHandle,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` API which incurs less latency compared to the `https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` API that executes the whole operation in one call.

| Parameters ||
|---|---|
| `request` | [GetCredentialRequest](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest): the request specifying type(s) of credentials to get from the user. This value cannot be `null`. |
| `cancellationSignal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#)?: an optional signal that allows for cancelling this call. This value may be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the callback will take place on this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| --- | --- |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [PrepareGetCredentialResponse](https://developer.android.com/reference/kotlin/android/credentials/PrepareGetCredentialResponse)!, [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException)!\>: the callback invoked when the request succeeds or fails. This value cannot be `null`. |

### registerCredentialDescription

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerCredentialDescription(request: RegisterCredentialDescriptionRequest): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription` for an actively provisioned `https://developer.android.com/reference/kotlin/android/credentials/Credential` a CredentialProvider has. This registry will then be used to determine where to fetch the requested `https://developer.android.com/reference/kotlin/android/credentials/Credential` from. Not all credential types will be supported. The distinction will be made by the JetPack layer. For the types that are supported, JetPack will add a new key-value pair into `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest`. These will not be persistent on the device. The Credential Providers will need to call this API again upon device reboot.

| Parameters ||
|---|---|
| `request` | [RegisterCredentialDescriptionRequest](https://developer.android.com/reference/kotlin/android/credentials/RegisterCredentialDescriptionRequest): the request data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the calling Credential Provider can not handle one or more of the Credential Types that are sent for registration. |
| `java.lang.UnsupportedOperationException` | if the feature has not been enabled. |

### unregisterCredentialDescription

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterCredentialDescription(request: UnregisterCredentialDescriptionRequest): Unit
```

Unregisters a `https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription` for an actively provisioned `https://developer.android.com/reference/kotlin/android/credentials/Credential` that has been registered previously.

| Parameters ||
|---|---|
| `request` | [UnregisterCredentialDescriptionRequest](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest): the request data. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the feature has not been enabled. |
