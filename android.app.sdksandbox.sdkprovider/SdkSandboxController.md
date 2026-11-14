Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SdkSandboxController

```
open class SdkSandboxController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.sdksandbox.sdkprovider.SdkSandboxController](https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The SDK sandbox is no longer supported.

Controller that is used by SDK loaded in the sandbox to access information provided by the sdk sandbox.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#SDK_SANDBOX_CONTROLLER_SERVICE:kotlin.String` <br /> |

| Public methods ||
|---|---|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface.html#)!\> | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#getAppOwnedSdkSandboxInterfaces()()` Fetches all `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface.html#` that are registered by the app. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#getClientPackageName()()` Returns the package name of the client app. |
| open [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#getClientSharedPreferences()()` Returns `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` containing data synced from the client app. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SandboxedSdk](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk.html#)!\> | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#getSandboxedSdks()()` Fetches information about Sdks that are loaded in the sandbox. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(sdkName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, params: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk.html#!, https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException.html#!>)` Loads SDK in an SDK sandbox java process. |
| open [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#registerSdkSandboxActivityHandler(android.app.sdksandbox.sdkprovider.SdkSandboxActivityHandler)(sdkSandboxActivityHandler: https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler)` Returns an identifier for a `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler` after registering it. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#registerSdkSandboxClientImportanceListener(java.util.concurrent.Executor,%20android.app.sdksandbox.sdkprovider.SdkSandboxClientImportanceListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxClientImportanceListener)` Registers a listener to be notified of changes in the client's process importance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#unregisterSdkSandboxActivityHandler(android.app.sdksandbox.sdkprovider.SdkSandboxActivityHandler)(sdkSandboxActivityHandler: https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler)` Unregister an already registered `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#unregisterSdkSandboxClientImportanceListener(android.app.sdksandbox.sdkprovider.SdkSandboxClientImportanceListener)(listener: https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxClientImportanceListener)` Unregisters a listener previously registered. |

## Constants

### SDK_SANDBOX_CONTROLLER_SERVICE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SDK_SANDBOX_CONTROLLER_SERVICE: String
```

**Deprecated:** *Deprecated in Java.*

 Value: "sdk_sandbox_controller_service"

## Public methods

### getAppOwnedSdkSandboxInterfaces

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppOwnedSdkSandboxInterfaces(): MutableList<AppOwnedSdkSandboxInterface!>
```

**Deprecated:** *Deprecated in Java.*

Fetches all `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface.html#` that are registered by the app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface.html#!>` | This value cannot be `null`. |

### getClientPackageName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClientPackageName(): String
```

**Deprecated:** *Deprecated in Java.*

Returns the package name of the client app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getClientSharedPreferences

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClientSharedPreferences(): SharedPreferences
```

**Deprecated:** *Deprecated in Java.*

Returns `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` containing data synced from the client app.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` | This value cannot be `null`. |

### getSandboxedSdks

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSandboxedSdks(): MutableList<SandboxedSdk!>
```

**Deprecated:** *Deprecated in Java.*

Fetches information about Sdks that are loaded in the sandbox.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk.html#!>` | This value cannot be `null`. |

### loadSdk

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadSdk(
    sdkName: String, 
    params: Bundle, 
    executor: Executor, 
    receiver: OutcomeReceiver<SandboxedSdk!, LoadSdkException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Loads SDK in an SDK sandbox java process.

| Parameters ||
|---|---|
| `sdkName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `params` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [SandboxedSdk](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk.html#)!, [LoadSdkException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException.html#)!\>: This value cannot be `null`. |

### registerSdkSandboxActivityHandler

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 7](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerSdkSandboxActivityHandler(sdkSandboxActivityHandler: SdkSandboxActivityHandler): IBinder
```

**Deprecated:** *Deprecated in Java.*

Returns an identifier for a `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler` after registering it.

| Parameters ||
|---|---|
| `sdkSandboxActivityHandler` | [SdkSandboxActivityHandler](https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/IBinder.html#` | This value cannot be `null`. |

### registerSdkSandboxClientImportanceListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerSdkSandboxClientImportanceListener(
    executor: Executor, 
    listener: SdkSandboxClientImportanceListener
): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers a listener to be notified of changes in the client's process importance.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [SdkSandboxClientImportanceListener](https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxClientImportanceListener): This value cannot be `null`. |

### unregisterSdkSandboxActivityHandler

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 7](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterSdkSandboxActivityHandler(sdkSandboxActivityHandler: SdkSandboxActivityHandler): Unit
```

**Deprecated:** *Deprecated in Java.*

Unregister an already registered `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler`.

| Parameters ||
|---|---|
| `sdkSandboxActivityHandler` | [SdkSandboxActivityHandler](https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxActivityHandler): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | This value cannot be `null`. |

### unregisterSdkSandboxClientImportanceListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterSdkSandboxClientImportanceListener(listener: SdkSandboxClientImportanceListener): Unit
```

**Deprecated:** *Deprecated in Java.*

Unregisters a listener previously registered.

| Parameters ||
|---|---|
| `listener` | [SdkSandboxClientImportanceListener](https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxClientImportanceListener): This value cannot be `null`. |
