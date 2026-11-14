Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SdkSandboxController

```
open class SdkSandboxController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.sdksandbox.sdkprovider.SdkSandboxController](SdkSandboxController.md) |

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
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppOwnedSdkSandboxInterface](../android.app.sdksandbox/AppOwnedSdkSandboxInterface.md)!\> | getAppOwnedSdkSandboxInterfaces Fetches all `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface.html#` that are registered by the app. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getClientPackageName Returns the package name of the client app. |
| open [SharedPreferences](../android.content/SharedPreferences.md) | getClientSharedPreferences Returns `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` containing data synced from the client app. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SandboxedSdk](../android.app.sdksandbox/SandboxedSdk.md)!\> | getSandboxedSdks Fetches information about Sdks that are loaded in the sandbox. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | loadSdk Loads SDK in an SDK sandbox java process. |
| open [IBinder](../android.os/IBinder.md) | registerSdkSandboxActivityHandler Returns an identifier for a SdkSandboxActivityHandler after registering it. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerSdkSandboxClientImportanceListener Registers a listener to be notified of changes in the client's process importance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterSdkSandboxActivityHandler Unregister an already registered SdkSandboxActivityHandler. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterSdkSandboxClientImportanceListener Unregisters a listener previously registered. |
| --- | --- |

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
| `params` | [Bundle](../android.os/Bundle.md): This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| --- | --- |
| `receiver` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [SandboxedSdk](../android.app.sdksandbox/SandboxedSdk.md)!, [LoadSdkException](../android.app.sdksandbox/LoadSdkException.md)!\>: This value cannot be `null`. |

### registerSdkSandboxActivityHandler

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 7](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun registerSdkSandboxActivityHandler(sdkSandboxActivityHandler: SdkSandboxActivityHandler): IBinder
```

**Deprecated:** *Deprecated in Java.*

Returns an identifier for a SdkSandboxActivityHandler after registering it.

| Parameters ||
|---|---|
| `sdkSandboxActivityHandler` | [SdkSandboxActivityHandler](SdkSandboxActivityHandler.md): This value cannot be `null`. |

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
| `executor` | [Executor](../java.util.concurrent/Executor.md): This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [SdkSandboxClientImportanceListener](SdkSandboxClientImportanceListener.md): This value cannot be `null`. |

### unregisterSdkSandboxActivityHandler

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 7](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregisterSdkSandboxActivityHandler(sdkSandboxActivityHandler: SdkSandboxActivityHandler): Unit
```

**Deprecated:** *Deprecated in Java.*

Unregister an already registered SdkSandboxActivityHandler.

| Parameters ||
|---|---|
| `sdkSandboxActivityHandler` | [SdkSandboxActivityHandler](SdkSandboxActivityHandler.md): This value cannot be `null`. |

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
| `listener` | [SdkSandboxClientImportanceListener](SdkSandboxClientImportanceListener.md): This value cannot be `null`. |
