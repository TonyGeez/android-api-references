# android.app.sdksandbox

# android.app.sdksandbox

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [SdkSandboxProcessDeathCallback](../android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback.md) | A callback for tracking events SDK sandbox death. |
| --- | --- |

## Classes

| [AppOwnedSdkSandboxInterface](AppOwnedSdkSandboxInterface.md) | Represents a channel for an SDK in the sandbox process to interact with the app. |
| --- | --- |
| [SandboxedSdk](SandboxedSdk.md) | Represents an SDK loaded in the sandbox process. |
| [SandboxedSdkProvider](SandboxedSdkProvider.md) | Encapsulates API which SDK sandbox can use to interact with SDKs loaded into it. |
| [SdkSandboxManager](SdkSandboxManager.md) | Provides APIs to load [SDKs](../android.content.pm/SharedLibraryInfo.md) into the SDK sandbox process, and then interact with them. |
| --- | --- |

## Exceptions

| [LoadSdkException](LoadSdkException.md) | Exception thrown by [SdkSandboxManager.loadSdk](SdkSandboxManager.md)) |
| --- | --- |
| [RequestSurfacePackageException](RequestSurfacePackageException.md) | Exception thrown by [SdkSandboxManager.requestSurfacePackage](SdkSandboxManager.md)) |
