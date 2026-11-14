Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions)

# SdkSandboxClientImportanceListener

Kotlin | [Java](SdkSandboxClientImportanceListener.md)
| --- | --- |

```
interface SdkSandboxClientImportanceListener
```

| [android.app.sdksandbox.sdkprovider.SdkSandboxClientImportanceListener](SdkSandboxClientImportanceListener.md) |

Used to notify the SDK about changes in the client's `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo.html#importance:kotlin.Int`.

When an SDK wants to get notified about changes in client's importance, it should register an implementation of this interface by calling registerSdkSandboxClientImportanceListener.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onForegroundImportanceChanged Invoked every time the client transitions from a value \<= `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo.html#IMPORTANCE_FOREGROUND:kotlin.Int` to a higher value or vice versa |

## Public methods

### onForegroundImportanceChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 14](https://developer.android.com/sdkExtensions)

```
abstract fun onForegroundImportanceChanged(isForeground: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Invoked every time the client transitions from a value \<= `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo.html#IMPORTANCE_FOREGROUND:kotlin.Int` to a higher value or vice versa

| Parameters ||
|---|---|
| `isForeground` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true when the client transitions to `https://developer.android.com/reference/kotlin/android/app/ActivityManager.RunningAppProcessInfo.html#IMPORTANCE_FOREGROUND:kotlin.Int` or lower and false when it is the other way round. |
