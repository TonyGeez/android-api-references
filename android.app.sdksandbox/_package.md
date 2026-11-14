# android.app.sdksandbox

# android.app.sdksandbox

Kotlin| [Java](../android/app/sdksandbox/_package.md)
| --- | --- |

## Interfaces

| [SdkSandboxProcessDeathCallback](../android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback.md) | A callback for tracking events SDK sandbox death. |
| --- | --- |

## Classes

| [AppOwnedSdkSandboxInterface](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md) | Represents a channel for an SDK in the sandbox process to interact with the app. |
| --- | --- |
| [SandboxedSdk](../android/app/sdksandbox/SandboxedSdk.md) | Represents an SDK loaded in the sandbox process. |
| [SandboxedSdkProvider](../android/app/sdksandbox/SandboxedSdkProvider.md) | Encapsulates API which SDK sandbox can use to interact with SDKs loaded into it. |
| [SdkSandboxManager](../android/app/sdksandbox/SdkSandboxManager.md) | Provides APIs to load [SDKs](../android/content/pm/SharedLibraryInfo.md) into the SDK sandbox process, and then interact with them. |
| --- | --- |

## Exceptions

| [LoadSdkException](../android/app/sdksandbox/LoadSdkException.md) | Exception thrown by [SdkSandboxManager.loadSdk](../android/app/sdksandbox/SdkSandboxManager.md)) |
| --- | --- |
| [RequestSurfacePackageException](../android/app/sdksandbox/RequestSurfacePackageException.md) | Exception thrown by [SdkSandboxManager.requestSurfacePackage](../android/app/sdksandbox/SdkSandboxManager.md)) |
