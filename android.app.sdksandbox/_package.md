# android.app.sdksandbox

# android.app.sdksandbox

Kotlin| [Java](https://developer.android.com/reference/android/app/sdksandbox/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [SdkSandboxProcessDeathCallback](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback) | A callback for tracking events SDK sandbox death. |
| --- | --- |

## Classes

| [AppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface) | Represents a channel for an SDK in the sandbox process to interact with the app. |
| --- | --- |
| [SandboxedSdk](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk) | Represents an SDK loaded in the sandbox process. |
| [SandboxedSdkProvider](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdkProvider) | Encapsulates API which SDK sandbox can use to interact with SDKs loaded into it. |
| [SdkSandboxManager](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager) | Provides APIs to load [SDKs](https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo.html#TYPE_SDK_PACKAGE:kotlin.Int) into the SDK sandbox process, and then interact with them. |
| --- | --- |

## Exceptions

| [LoadSdkException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException) | Exception thrown by [SdkSandboxManager.loadSdk](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)) |
| --- | --- |
| [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException) | Exception thrown by [SdkSandboxManager.requestSurfacePackage](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)) |
