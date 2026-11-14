# MediaQualityManager.AmbientBacklightCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AmbientBacklightCallback

Kotlin| [Java](https://developer.android.com/reference/android/media/quality/MediaQualityManager.AmbientBacklightCallback "View this page in Java") 
| --- | --- |

```
interface AmbientBacklightCallback
```

| [android.media.quality.MediaQualityManager.AmbientBacklightCallback](https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.AmbientBacklightCallback#) |

Callback used to monitor status of ambient backlight.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAmbientBacklightEvent](https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityManager.AmbientBacklightCallback#onAmbientBacklightEvent(android.media.quality.AmbientBacklightEvent))`(`event:` ` [AmbientBacklightEvent](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent)`)` Called when new ambient backlight event is emitted. |

## Public methods

### onAmbientBacklightEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAmbientBacklightEvent(event: AmbientBacklightEvent): Unit
```

Called when new ambient backlight event is emitted.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AmbientBacklightEvent](https://developer.android.com/reference/kotlin/android/media/quality/AmbientBacklightEvent):This value cannot be`null`. |
