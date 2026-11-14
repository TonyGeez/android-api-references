# DrmManagerClient.OnErrorListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnErrorListener

Kotlin| [Java](../android/drm/DrmManagerClient.OnErrorListener.md) 
| --- | --- |

```
interface OnErrorListener
```

| [android.drm.DrmManagerClient.OnErrorListener](../android/drm/DrmManagerClient.OnErrorListener.md) |

| **This interface was deprecated in API level 30.**
|
| Deprecated in Java.

Interface definition for a callback that receives information about DRM framework errors.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](../android/drm/DrmManagerClient.OnErrorListener.md))`(`client:` ` [DrmManagerClient](DrmManagerClient.md)!`, `event:` ` [DrmErrorEvent](DrmErrorEvent.md)!`)` Called when the DRM framework sends error information. |

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
| `client` | [DrmManagerClient](DrmManagerClient.md)!:The`DrmManagerClient`instance. |
| `event` | [DrmErrorEvent](DrmErrorEvent.md)!:The [DrmErrorEvent](DrmErrorEvent.md) instance that wraps the error type and message. |
