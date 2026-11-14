# VoiceInteractionSession.VisibleActivityCallback

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VisibleActivityCallback

Kotlin| [Java](../android/service/voice/VoiceInteractionSession.VisibleActivityCallback.md) 
| --- | --- |

```
interface VisibleActivityCallback
```

| [android.service.voice.VoiceInteractionSession.VisibleActivityCallback](../android/service/voice/VoiceInteractionSession.VisibleActivityCallback.md) |

Callback interface for receiving visible activity changes used for assistant usage.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInvisible](../android/service/voice/VoiceInteractionSession.VisibleActivityCallback.md))`(`activityId:` ` [VoiceInteractionSession.ActivityId](../android/service/voice/VoiceInteractionSession.ActivityId.md)`)` Callback to inform that a visible activity has gone. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVisible](../android/service/voice/VoiceInteractionSession.VisibleActivityCallback.md))`(`activityInfo:` ` [VisibleActivityInfo](../android/service/voice/VisibleActivityInfo.md)`)` Callback to inform that an activity has become visible. |

## Public methods

### onInvisible

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInvisible(activityId: VoiceInteractionSession.ActivityId): Unit
```

Callback to inform that a visible activity has gone.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activityId` | [VoiceInteractionSession.ActivityId](../android/service/voice/VoiceInteractionSession.ActivityId.md):This value cannot be`null`. |

### onVisible

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onVisible(activityInfo: VisibleActivityInfo): Unit
```

Callback to inform that an activity has become visible.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `activityInfo` | [VisibleActivityInfo](../android/service/voice/VisibleActivityInfo.md):This value cannot be`null`. |
