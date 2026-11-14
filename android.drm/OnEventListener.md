# DrmManagerClient.OnEventListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnEventListener

Kotlin| [Java](../android/drm/DrmManagerClient.OnEventListener.md) 
| --- | --- |

```
interface OnEventListener
```

| [android.drm.DrmManagerClient.OnEventListener](../android/drm/DrmManagerClient.OnEventListener.md) |

| **This interface was deprecated in API level 30.**
|
| Deprecated in Java.

Interface definition for a callback that receives information about DRM processing events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEvent](../android/drm/DrmManagerClient.OnEventListener.md))`(`client:` ` [DrmManagerClient](../android/drm/DrmManagerClient.md)!`, `event:` ` [DrmEvent](../android/drm/DrmEvent.md)!`)` Called when the DRM framework sends information about a DRM processing request. |

## Public methods

### onEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEvent(
    client: DrmManagerClient!, 
    event: DrmEvent!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the DRM framework sends information about a DRM processing request.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `client` | [DrmManagerClient](../android/drm/DrmManagerClient.md)!:The`DrmManagerClient`instance. |
| `event` | [DrmEvent](../android/drm/DrmEvent.md)!:The [DrmEvent](../android/drm/DrmEvent.md) instance that wraps the information being conveyed, such as the information type and message. |
