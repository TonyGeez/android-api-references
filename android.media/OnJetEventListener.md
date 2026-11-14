# JetPlayer.OnJetEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnJetEventListener

Kotlin| [Java](../android/media/JetPlayer.OnJetEventListener.md) 
| --- | --- |

```
interface OnJetEventListener
```

| [android.media.JetPlayer.OnJetEventListener](../android/media/JetPlayer.OnJetEventListener.md) |

Handles the notification when the JET engine generates an event.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onJetEvent](../android/media/JetPlayer.OnJetEventListener.md))`(`player:` ` [JetPlayer](../android/media/JetPlayer.md)!`, `segment:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `track:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `channel:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `controller:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `value:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Callback for when the JET engine generates a new event. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onJetNumQueuedSegmentUpdate](../android/media/JetPlayer.OnJetEventListener.md))`(`player:` ` [JetPlayer](../android/media/JetPlayer.md)!`, `nbSegments:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback for when JET's number of queued segments is updated. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onJetPauseUpdate](../android/media/JetPlayer.OnJetEventListener.md))`(`player:` ` [JetPlayer](../android/media/JetPlayer.md)!`, `paused:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback for when JET pause state is updated. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onJetUserIdUpdate](../android/media/JetPlayer.OnJetEventListener.md))`(`player:` ` [JetPlayer](../android/media/JetPlayer.md)!`, `userId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback for when JET's currently playing segment's userID is updated. |

## Public methods

### onJetEvent

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onJetEvent(
    player: JetPlayer!, 
    segment: Short, 
    track: Byte, 
    channel: Byte, 
    controller: Byte, 
    value: Byte
): Unit
```

Callback for when the JET engine generates a new event.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------|
| `player` | [JetPlayer](../android/media/JetPlayer.md)!:the JET player the event is coming from |
| `segment` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):8 bit unsigned value |
| `track` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):6 bit unsigned value |
| --- | --- |
| `channel` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):4 bit unsigned value |
| `controller` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):7 bit unsigned value |
| `value` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):7 bit unsigned value |
| --- | --- |

### onJetNumQueuedSegmentUpdate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onJetNumQueuedSegmentUpdate(
    player: JetPlayer!, 
    nbSegments: Int
): Unit
```

Callback for when JET's number of queued segments is updated.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `player` | [JetPlayer](../android/media/JetPlayer.md)!:the JET player the status update is coming from |
| `nbSegments` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of segments in the JET queue |

### onJetPauseUpdate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onJetPauseUpdate(
    player: JetPlayer!, 
    paused: Int
): Unit
```

Callback for when JET pause state is updated.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `player` | [JetPlayer](../android/media/JetPlayer.md)!:the JET player the status update is coming from |
| `paused` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):indicates whether JET is paused (1) or not (0) |

### onJetUserIdUpdate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onJetUserIdUpdate(
    player: JetPlayer!, 
    userId: Int, 
    repeatCount: Int
): Unit
```

Callback for when JET's currently playing segment's userID is updated.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `player` | [JetPlayer](../android/media/JetPlayer.md)!:the JET player the status update is coming from |
| `userId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the ID of the currently playing segment |
| `repeatCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the repetition count for the segment (0 means it plays once) |
| --- | --- |
