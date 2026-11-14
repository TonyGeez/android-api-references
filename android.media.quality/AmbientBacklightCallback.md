# MediaQualityManager.AmbientBacklightCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AmbientBacklightCallback

Kotlin| [Java](../android/media/quality/MediaQualityManager.AmbientBacklightCallback.md) 
| --- | --- |

```
interface AmbientBacklightCallback
```

| [android.media.quality.MediaQualityManager.AmbientBacklightCallback](../android/media/quality/MediaQualityManager.AmbientBacklightCallback.md) |

Callback used to monitor status of ambient backlight.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAmbientBacklightEvent](../android/media/quality/MediaQualityManager.AmbientBacklightCallback.md))`(`event:` ` [AmbientBacklightEvent](AmbientBacklightEvent.md)`)` Called when new ambient backlight event is emitted. |

## Public methods

### onAmbientBacklightEvent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAmbientBacklightEvent(event: AmbientBacklightEvent): Unit
```

Called when new ambient backlight event is emitted.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AmbientBacklightEvent](AmbientBacklightEvent.md):This value cannot be`null`. |
