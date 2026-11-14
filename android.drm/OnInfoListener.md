# DrmManagerClient.OnInfoListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnInfoListener

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmManagerClient.OnInfoListener "View this page in Java") 

```
interface OnInfoListener
```

| [android.drm.DrmManagerClient.OnInfoListener](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener#) |

| **This interface was deprecated in API level 30.**
|
| Deprecated in Java.

Interface definition for a callback that receives status messages and warnings during registration and rights acquisition.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInfo](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient.OnInfoListener#onInfo(android.drm.DrmManagerClient,%20android.drm.DrmInfoEvent))`(`client:` ` [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient)!`, `event:` ` [DrmInfoEvent](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent)!`)` Called when the DRM framework sends status or warning information during registration and rights acquisition. |

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
| `client` | [DrmManagerClient](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient)!:The`DrmManagerClient`instance. |
| `event` | [DrmInfoEvent](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent)!:The [DrmInfoEvent](https://developer.android.com/reference/kotlin/android/drm/DrmInfoEvent) instance that wraps the status information or warnings. |
