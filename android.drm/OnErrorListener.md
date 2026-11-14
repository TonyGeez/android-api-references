# DrmManagerClient.OnErrorListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnErrorListener

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmManagerClient.OnErrorListener "View this page in Java") 
| --- | --- |

```
interface OnErrorListener
```

| [android.drm.DrmManagerClient.OnErrorListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener#) |

| **This interface was deprecated in API level 30.**
|
| Deprecated in Java.

Interface definition for a callback that receives information about DRM framework errors.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnErrorListener#onError(android.drm.DrmManagerClient,%20android.drm.DrmErrorEvent))`(`client:` ` [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient)!`, `event:` ` [DrmErrorEvent](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent)!`)` Called when the DRM framework sends error information. |

## Public methods

### onError

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(
    client: DrmManagerClient!, 
    event: DrmErrorEvent!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the DRM framework sends error information.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `client` | [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient)!:The`DrmManagerClient`instance. |
| `event` | [DrmErrorEvent](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent)!:The [DrmErrorEvent](https://developer.android.com/reference/kotlin/android/drm/DrmErrorEvent) instance that wraps the error type and message. |
