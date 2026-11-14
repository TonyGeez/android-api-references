# DrmManagerClient.OnInfoListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnInfoListener

Kotlin| [Java](../android/drm/DrmManagerClient.OnInfoListener.md) 
| --- | --- |

```
interface OnInfoListener
```

| [android.drm.DrmManagerClient.OnInfoListener](../android/drm/DrmManagerClient.OnInfoListener.md) |

| **This interface was deprecated in API level 30.**
|
| Deprecated in Java.

Interface definition for a callback that receives status messages and warnings during registration and rights acquisition.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInfo](../android/drm/DrmManagerClient.OnInfoListener.md))`(`client:` ` [DrmManagerClient](../android/drm/DrmManagerClient.md)!`, `event:` ` [DrmInfoEvent](../android/drm/DrmInfoEvent.md)!`)` Called when the DRM framework sends status or warning information during registration and rights acquisition. |

## Public methods

### onInfo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInfo(
    client: DrmManagerClient!, 
    event: DrmInfoEvent!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the DRM framework sends status or warning information during registration and rights acquisition.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `client` | [DrmManagerClient](../android/drm/DrmManagerClient.md)!:The`DrmManagerClient`instance. |
| `event` | [DrmInfoEvent](../android/drm/DrmInfoEvent.md)!:The [DrmInfoEvent](../android/drm/DrmInfoEvent.md) instance that wraps the status information or warnings. |
