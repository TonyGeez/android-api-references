# DrmManagerClient.OnEventListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnEventListener

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmManagerClient.OnEventListener "View this page in Java") 
| --- | --- |

```
interface OnEventListener
```

| [android.drm.DrmManagerClient.OnEventListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnEventListener#) |

| **This interface was deprecated in API level 30.**
|
| Deprecated in Java.

Interface definition for a callback that receives information about DRM processing events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEvent](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnEventListener#onEvent(android.drm.DrmManagerClient,%20android.drm.DrmEvent))`(`client:` ` [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient)!`, `event:` ` [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent)!`)` Called when the DRM framework sends information about a DRM processing request. |

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
| `client` | [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient)!:The`DrmManagerClient`instance. |
| `event` | [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent)!:The [DrmEvent](https://developer.android.com/reference/kotlin/android/drm/DrmEvent) instance that wraps the information being conveyed, such as the information type and message. |
