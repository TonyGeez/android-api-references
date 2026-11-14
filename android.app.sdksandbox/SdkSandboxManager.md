Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 3](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SdkSandboxManager

```
class SdkSandboxManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.sdksandbox.SdkSandboxManager](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The SDK sandbox is no longer supported.

Provides APIs to load `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo.html#TYPE_SDK_PACKAGE:kotlin.Int` into the SDK sandbox process, and then interact with them.

SDK sandbox is a java process running in a separate uid range. Each app may have its own SDK sandbox process.

The app first needs to declare SDKs it depends on in its manifest using the `<uses-sdk-library>` tag. Apps may only load SDKs they depend on into the SDK sandbox.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback` A callback for tracking events SDK sandbox death. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_DISPLAY_ID:kotlin.String` The name of key to be used in the Bundle fields of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value should define the integer ID of the logical display to display the SurfacePackage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_HEIGHT_IN_PIXELS:kotlin.String` The name of key to be used in the Bundle fields of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value should define the integer height of the SurfacePackage in pixels. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_HOST_TOKEN:kotlin.String` The name of key to be used in the Bundle fields of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value should present the token returned by `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#getHostToken()` once the `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` has been added to the view hierarchy. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_SURFACE_PACKAGE:kotlin.String` The name of key in the Bundle which is passed to the `onResult` function of the `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#` which is field of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value presents the requested SurfacePackage. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_WIDTH_IN_PIXELS:kotlin.String` The name of key to be used in the Bundle fields of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value should define the integer width of the SurfacePackage in pixels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_ALREADY_LOADED:kotlin.Int` SDK is already loaded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_INTERNAL_ERROR:kotlin.Int` Internal error while loading SDK. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_NOT_FOUND:kotlin.Int` SDK not found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_SDK_DEFINED_ERROR:kotlin.Int` SDK error after being loaded. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_SDK_SANDBOX_DISABLED:kotlin.Int` SDK sandbox is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR:kotlin.Int` Internal error while requesting a SurfacePackage. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED:kotlin.Int` SDK is not loaded while requesting a SurfacePackage. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#SDK_SANDBOX_PROCESS_NOT_AVAILABLE:kotlin.Int` SDK sandbox process is not available. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#SDK_SANDBOX_SERVICE:kotlin.String` Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#` for interacting with the SDKs belonging to this client application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#SDK_SANDBOX_STATE_DISABLED:kotlin.Int` SDK sandbox is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#SDK_SANDBOX_STATE_ENABLED_PROCESS_ISOLATION:kotlin.Int` SDK sandbox is enabled. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#addSdkSandboxProcessDeathCallback(java.util.concurrent.Executor,%20android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback)(callbackExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback)` Adds a callback which gets registered for SDK sandbox lifecycle events, such as SDK sandbox death. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#addSyncedSharedPreferencesKeys(kotlin.collections.MutableSet)(keys: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Adds keys to set of keys being synced from app's default `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` to the SDK sandbox. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface)!\> | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#getAppOwnedSdkSandboxInterfaces()()` Fetches a list of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface` registered for an app |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SandboxedSdk](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk)!\> | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#getSandboxedSdks()()` Fetches information about SDKs that are loaded in the sandbox. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#getSdkSandboxState()()` Returns the current state of the availability of the SDK sandbox feature. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#getSyncedSharedPreferencesKeys()()` Returns the set keys that are being synced from app's default `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` to the SDK sandbox. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(sdkName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, params: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk!, https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException!>)` Loads SDK in an SDK sandbox java process. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#registerAppOwnedSdkSandboxInterface(android.app.sdksandbox.AppOwnedSdkSandboxInterface)(appOwnedSdkSandboxInterface: https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface)` Registers `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface` for an app process. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#removeSdkSandboxProcessDeathCallback(android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback)(callback: https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback)` Removes an `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback` that was previously added using `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#addSdkSandboxProcessDeathCallback(java.util.concurrent.Executor,%20android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback)` |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#removeSyncedSharedPreferencesKeys(kotlin.collections.MutableSet)(keys: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Removes keys from set of keys that have been added using `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#addSyncedSharedPreferencesKeys(kotlin.collections.MutableSet)` |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(sdkName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, params: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, callbackExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, receiver: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException!>)` Sends a request for a surface package to the SDK. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#startSdkSandboxActivity(android.app.Activity,%20android.os.IBinder)(fromActivity: https://developer.android.com/reference/kotlin/android/app/Activity.html#, sdkActivityToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#)` Starts an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` in the SDK sandbox. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#unloadSdk(kotlin.String)(sdkName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Unloads an SDK that has been previously loaded by the caller. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#unregisterAppOwnedSdkSandboxInterface(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Unregisters `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface`s for an app process. |

## Constants

### EXTRA_DISPLAY_ID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DISPLAY_ID: String
```

**Deprecated:** *Parameter for `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` which is getting deprecated.*

The name of key to be used in the Bundle fields of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value should define the integer ID of the logical display to display the SurfacePackage.

 Value: "android.app.sdksandbox.extra.DISPLAY_ID"

### EXTRA_HEIGHT_IN_PIXELS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_HEIGHT_IN_PIXELS: String
```

**Deprecated:** *Parameter for `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` which is getting deprecated.*

The name of key to be used in the Bundle fields of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value should define the integer height of the SurfacePackage in pixels.

 Value: "android.app.sdksandbox.extra.HEIGHT_IN_PIXELS"

### EXTRA_HOST_TOKEN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_HOST_TOKEN: String
```

**Deprecated:** *Parameter for `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` which is getting deprecated.*

The name of key to be used in the Bundle fields of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value should present the token returned by `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#getHostToken()` once the `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` has been added to the view hierarchy. Only a non-null value is accepted to enable ANR reporting.

 Value: "android.app.sdksandbox.extra.HOST_TOKEN"

### EXTRA_SURFACE_PACKAGE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SURFACE_PACKAGE: String
```

**Deprecated:** *Parameter for `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` which is getting deprecated.*

The name of key in the Bundle which is passed to the `onResult` function of the `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#` which is field of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value presents the requested SurfacePackage.

 Value: "android.app.sdksandbox.extra.SURFACE_PACKAGE"

### EXTRA_WIDTH_IN_PIXELS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_WIDTH_IN_PIXELS: String
```

**Deprecated:** *Parameter for `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` which is getting deprecated.*

The name of key to be used in the Bundle fields of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, its value should define the integer width of the SurfacePackage in pixels.

 Value: "android.app.sdksandbox.extra.WIDTH_IN_PIXELS"

### LOAD_SDK_ALREADY_LOADED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOAD_SDK_ALREADY_LOADED: Int
```

**Deprecated:** *Deprecated in Java.*

SDK is already loaded.

This indicates that client application tried to reload the same SDK by calling `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` after being successfully loaded.

 Value: 101

### LOAD_SDK_INTERNAL_ERROR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOAD_SDK_INTERNAL_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

Internal error while loading SDK.

This indicates a generic internal error happened while applying the call from client application.

 Value: 500

### LOAD_SDK_NOT_FOUND

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOAD_SDK_NOT_FOUND: Int
```

**Deprecated:** *Deprecated in Java.*

SDK not found.

This indicates that client application tried to load a non-existing SDK by calling `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

 Value: 100

### LOAD_SDK_SDK_DEFINED_ERROR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOAD_SDK_SDK_DEFINED_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

SDK error after being loaded.

This indicates that the SDK encountered an error during post-load initialization. The details of this can be obtained from the Bundle returned in `https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException` through the `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#` passed in to `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

 Value: 102

### LOAD_SDK_SDK_SANDBOX_DISABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOAD_SDK_SDK_SANDBOX_DISABLED: Int
```

**Deprecated:** *Deprecated in Java.*

SDK sandbox is disabled.

This indicates that the SDK sandbox is disabled. Any subsequent attempts to load SDKs in this boot will also fail.

 Value: 103

### REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

Internal error while requesting a SurfacePackage.

This indicates a generic internal error happened while requesting a SurfacePackage.

 Value: 700

### REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED: Int
```

**Deprecated:** *Deprecated in Java.*

SDK is not loaded while requesting a SurfacePackage.

This indicates that the SDK for which the SurfacePackage is being requested is not loaded, either because the sandbox died or because it was not loaded in the first place.

 Value: 701

### SDK_SANDBOX_PROCESS_NOT_AVAILABLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SDK_SANDBOX_PROCESS_NOT_AVAILABLE: Int
```

**Deprecated:** *Deprecated in Java.*

SDK sandbox process is not available.

This indicates that the SDK sandbox process is not available, either because it has died, disconnected or was not created in the first place.

 Value: 503

### SDK_SANDBOX_SERVICE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SDK_SANDBOX_SERVICE: String
```

**Deprecated:** *Deprecated in Java.*

Use with `https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String)` to retrieve an `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#` for interacting with the SDKs belonging to this client application.

 Value: "sdk_sandbox"

### SDK_SANDBOX_STATE_DISABLED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 3](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SDK_SANDBOX_STATE_DISABLED: Int
```

**Deprecated:** *Deprecated in Java.*

SDK sandbox is disabled.

`https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#` APIs are hidden. Attempts at calling them will result in `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

 Value: 0

### SDK_SANDBOX_STATE_ENABLED_PROCESS_ISOLATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 3](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SDK_SANDBOX_STATE_ENABLED_PROCESS_ISOLATION: Int
```

**Deprecated:** *Deprecated in Java.*

SDK sandbox is enabled.

App can use `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#` APIs to load `SDKs` it depends on into the corresponding SDK sandbox process.

 Value: 2

## Public methods

### addSdkSandboxProcessDeathCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addSdkSandboxProcessDeathCallback(
    callbackExecutor: Executor, 
    callback: SdkSandboxManager.SdkSandboxProcessDeathCallback
): Unit
```

**Deprecated:** *Deprecated in Java.*

Adds a callback which gets registered for SDK sandbox lifecycle events, such as SDK sandbox death. If the sandbox has not yet been created when this is called, the request will be stored until a sandbox is created, at which point it is activated for that sandbox. Multiple callbacks can be added to detect death and will not be removed when the sandbox dies.

| Parameters ||
|---|---|
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [SdkSandboxManager.SdkSandboxProcessDeathCallback](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback): the `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback` which will receive SDK sandbox lifecycle events. This value cannot be `null`. |

### addSyncedSharedPreferencesKeys

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addSyncedSharedPreferencesKeys(keys: MutableSet<String!>): Unit
```

**Deprecated:** *Deprecated in Java.*

Adds keys to set of keys being synced from app's default `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` to the SDK sandbox.

Synced data will be available for SDKs to read using the `https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#getClientSharedPreferences()` API.

To stop syncing any key that has been added using this API, use `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#removeSyncedSharedPreferencesKeys(kotlin.collections.MutableSet)`.

The sync breaks if the app restarts and user must call this API again to rebuild the pool of keys for syncing.

Note: This class does not support use across multiple processes.

| Parameters ||
|---|---|
| `keys` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: set of keys that will be synced to Sandbox. This value cannot be `null`. |

### getAppOwnedSdkSandboxInterfaces

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAppOwnedSdkSandboxInterfaces(): MutableList<AppOwnedSdkSandboxInterface!>
```

**Deprecated:** *Deprecated in Java.*

Fetches a list of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface` registered for an app

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface!>` | empty list if callingInfo not found in map otherwise a list of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface` This value cannot be `null`. |

### getSandboxedSdks

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSandboxedSdks(): MutableList<SandboxedSdk!>
```

**Deprecated:** *Deprecated in Java.*

Fetches information about SDKs that are loaded in the sandbox.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk!>` | List of `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk` containing all currently loaded SDKs. This value cannot be `null`. |

### getSdkSandboxState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 3](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSdkSandboxState(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the current state of the availability of the SDK sandbox feature.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#SDK_SANDBOX_STATE_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#SDK_SANDBOX_STATE_ENABLED_PROCESS_ISOLATION:kotlin.Int` |

### getSyncedSharedPreferencesKeys

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSyncedSharedPreferencesKeys(): MutableSet<String!>
```

**Deprecated:** *Deprecated in Java.*

Returns the set keys that are being synced from app's default `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` to the SDK sandbox.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### loadSdk

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun loadSdk(
    sdkName: String, 
    params: Bundle, 
    executor: Executor, 
    receiver: OutcomeReceiver<SandboxedSdk!, LoadSdkException!>
): Unit
```

**Deprecated:** *Deprecated in Java.*

Loads SDK in an SDK sandbox java process.

Loads SDK library with `sdkName` to an SDK sandbox process asynchronously. The caller will be notified through the `receiver`.

The caller should already declare `SDKs` it depends on in its manifest using `<uses-sdk-library>` tag. The caller may only load `SDKs` it depends on into the SDK sandbox.

When the client application loads the first SDK, a new SDK sandbox process will be created. If a sandbox has already been created for the client application, additional SDKs will be loaded into the same sandbox.

This API may only be called while the caller is running in the foreground. Calls from the background will result in returning `https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException` in the `receiver`.

| Parameters ||
|---|---|
| `sdkName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name of the SDK to be loaded. This value cannot be `null`. |
| `params` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): additional parameters to be passed to the SDK in the form of a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` as agreed between the client and the SDK. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the receiver. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [SandboxedSdk](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk)!, [LoadSdkException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException)!\>: This either receives a `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk` on a successful run, or `https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException`. This value cannot be `null`. |

### registerAppOwnedSdkSandboxInterface

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerAppOwnedSdkSandboxInterface(appOwnedSdkSandboxInterface: AppOwnedSdkSandboxInterface): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface` for an app process.

Registering an `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface` that has same name as a previously registered interface will result in `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

`https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#getName()` refers to the name of the interface.

| Parameters ||
|---|---|
| `appOwnedSdkSandboxInterface` | [AppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface): the AppOwnedSdkSandboxInterface to be registered. This value cannot be `null`. |

### removeSdkSandboxProcessDeathCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeSdkSandboxProcessDeathCallback(callback: SdkSandboxManager.SdkSandboxProcessDeathCallback): Unit
```

**Deprecated:** *Deprecated in Java.*

Removes an `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback` that was previously added using `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#addSdkSandboxProcessDeathCallback(java.util.concurrent.Executor,%20android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback)`

| Parameters ||
|---|---|
| `callback` | [SdkSandboxManager.SdkSandboxProcessDeathCallback](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback): the `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback` which was previously added using `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#addSdkSandboxProcessDeathCallback(java.util.concurrent.Executor,%20android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback)` This value cannot be `null`. |

### removeSyncedSharedPreferencesKeys

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeSyncedSharedPreferencesKeys(keys: MutableSet<String!>): Unit
```

**Deprecated:** *Deprecated in Java.*

Removes keys from set of keys that have been added using `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#addSyncedSharedPreferencesKeys(kotlin.collections.MutableSet)`

Removed keys will be erased from the SDK sandbox if they have been synced already.

| Parameters ||
|---|---|
| `keys` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: set of key names that should no longer be synced to Sandbox. This value cannot be `null`. |

### requestSurfacePackage

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun requestSurfacePackage(
    sdkName: String, 
    params: Bundle, 
    callbackExecutor: Executor, 
    receiver: OutcomeReceiver<Bundle!, RequestSurfacePackageException!>
): Unit
```

**Deprecated:** *This method will no longer be supported through `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#`. Please consider using androidx.privacysandbox library as an alternative*

Sends a request for a surface package to the SDK.

After the client application receives a signal about a successful SDK loading, and has added a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` to the view hierarchy, it may asynchronously request a SurfacePackage to render a view from the SDK.

When the SurfacePackage is ready, the `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#onResult(android.os.OutcomeReceiver.R)` callback of the passed `receiver` will be invoked. This callback will contain a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` object, which will contain the key `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_SURFACE_PACKAGE:kotlin.String` whose associated value is the requested SurfacePackage.

The passed `params` must contain the following keys: `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_WIDTH_IN_PIXELS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_HEIGHT_IN_PIXELS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_DISPLAY_ID:kotlin.String` and `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_HOST_TOKEN:kotlin.String`. If any of these keys are missing or invalid, an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

This API may only be called while the caller is running in the foreground. Calls from the background will result in returning RequestSurfacePackageException in the `receiver`.

| Parameters ||
|---|---|
| `sdkName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name of the SDK loaded into the SDK sandbox. This value cannot be `null`. |
| `params` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#): the parameters which the client application passes to the SDK. This value cannot be `null`. |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `receiver` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!, [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException)!\>: This either returns a `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` on success which will contain the key `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_SURFACE_PACKAGE:kotlin.String` with a SurfacePackage value, or `https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException` on failure. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `params` does not contain all required keys. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_WIDTH_IN_PIXELS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_HEIGHT_IN_PIXELS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_DISPLAY_ID:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#EXTRA_HOST_TOKEN:kotlin.String`

### startSdkSandboxActivity

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 7](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startSdkSandboxActivity(
    fromActivity: Activity, 
    sdkActivityToken: IBinder
): Unit
```

**Deprecated:** *Deprecated in Java.*

Starts an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` in the SDK sandbox.

This function will start a new `https://developer.android.com/reference/kotlin/android/app/Activity.html#` in the same task of the passed `fromActivity` and pass it to the SDK that shared the passed `sdkActivityToken` that identifies a request from that SDK to stat this `https://developer.android.com/reference/kotlin/android/app/Activity.html#`.

The `https://developer.android.com/reference/kotlin/android/app/Activity.html#` will not start in the following cases:

- The App calling this API is in the background.
- The passed `sdkActivityToken` does not map to a request for an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` form the SDK that shared it with the caller app.
- The SDK that shared the passed `sdkActivityToken` removed its request for this `https://developer.android.com/reference/kotlin/android/app/Activity.html#`.
- The sandbox `https://developer.android.com/reference/kotlin/android/app/Activity.html#` is already created.

| Parameters ||
|---|---|
| `fromActivity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#): the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` will be used to start the new sandbox `https://developer.android.com/reference/kotlin/android/app/Activity.html#` by calling android.app.Activity#startActivity(android.content.Intent) against it. This value cannot be `null`. |
| `sdkActivityToken` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#): the identifier that is shared by the SDK which requests the `https://developer.android.com/reference/kotlin/android/app/Activity.html#`. This value cannot be `null`. |

### unloadSdk

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unloadSdk(sdkName: String): Unit
```

**Deprecated:** *Deprecated in Java.*

Unloads an SDK that has been previously loaded by the caller.

It is not guaranteed that the memory allocated for this SDK will be freed immediately. All subsequent calls to `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` for the given `sdkName` will fail.

This API may only be called while the caller is running in the foreground. Calls from the background will result in a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#` being thrown.

| Parameters ||
|---|---|
| `sdkName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): name of the SDK to be unloaded. This value cannot be `null`. |

### unregisterAppOwnedSdkSandboxInterface

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterAppOwnedSdkSandboxInterface(name: String): Unit
```

**Deprecated:** *Deprecated in Java.*

Unregisters `https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface`s for an app process.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name under which AppOwnedSdkSandboxInterface was registered. This value cannot be `null`. |
