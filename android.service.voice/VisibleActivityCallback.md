# VoiceInteractionSession.VisibleActivityCallback

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VisibleActivityCallback

Kotlin| [Java](https://developer.android.com/reference/android/service/voice/VoiceInteractionSession.VisibleActivityCallback "View this page in Java") 
| --- | --- |

```
interface VisibleActivityCallback
```

| [android.service.voice.VoiceInteractionSession.VisibleActivityCallback](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.VisibleActivityCallback#) |

Callback interface for receiving visible activity changes used for assistant usage.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInvisible](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.VisibleActivityCallback#onInvisible(android.service.voice.VoiceInteractionSession.ActivityId))`(`activityId:` ` [VoiceInteractionSession.ActivityId](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ActivityId)`)` Callback to inform that a visible activity has gone. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVisible](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.VisibleActivityCallback#onVisible(android.service.voice.VisibleActivityInfo))`(`activityInfo:` ` [VisibleActivityInfo](https://developer.android.com/reference/kotlin/android/service/voice/VisibleActivityInfo)`)` Callback to inform that an activity has become visible. |

## Public methods

### onInvisible

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInvisible(activityId: VoiceInteractionSession.ActivityId): Unit
```

Callback to inform that a visible activity has gone.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activityId` | [VoiceInteractionSession.ActivityId](https://developer.android.com/reference/kotlin/android/service/voice/VoiceInteractionSession.ActivityId):This value cannot be`null`. |

### onVisible

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onVisible(activityInfo: VisibleActivityInfo): Unit
```

Callback to inform that an activity has become visible.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `activityInfo` | [VisibleActivityInfo](https://developer.android.com/reference/kotlin/android/service/voice/VisibleActivityInfo):This value cannot be`null`. |
