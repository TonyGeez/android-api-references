# SdkSandboxManager.SdkSandboxProcessDeathCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# SdkSandboxProcessDeathCallback

Kotlin| [Java](https://developer.android.com/reference/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback "View this page in Java") 
| --- | --- |

```
interface SdkSandboxProcessDeathCallback
```

| [android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback#) |

A callback for tracking events SDK sandbox death.

The callback can be added using [android.app.sdksandbox.SdkSandboxManager#addSdkSandboxProcessDeathCallback(java.util.concurrent.Executor,android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback)](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#addSdkSandboxProcessDeathCallback(java.util.concurrent.Executor,%20android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback))and removed using [android.app.sdksandbox.SdkSandboxManager#removeSdkSandboxProcessDeathCallback(android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback)](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#removeSdkSandboxProcessDeathCallback(android.app.sdksandbox.SdkSandboxManager.SdkSandboxProcessDeathCallback))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSdkSandboxDied](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager.SdkSandboxProcessDeathCallback#onSdkSandboxDied())`()` Notifies the client application that the SDK sandbox has died. |

## Public methods

### onSdkSandboxDied

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
abstract fun onSdkSandboxDied(): Unit
```

Notifies the client application that the SDK sandbox has died. The sandbox could die for various reasons, for example, due to memory pressure on the system, or a crash in the sandbox. The system will automatically restart the sandbox process if it died due to a crash. However, the state of the sandbox will be lost - so any SDKs that were loaded previously would have to be loaded again, using [SdkSandboxManager.loadSdk(String, Bundle,](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))to continue using them.
