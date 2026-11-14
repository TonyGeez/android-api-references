# MediaCas.EventListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventListener

Kotlin| [Java](../android/media/MediaCas.EventListener.md) 
| --- | --- |

```
interface EventListener
```

| [android.media.MediaCas.EventListener](../android/media/MediaCas.EventListener.md) |

An interface registered by the caller to [setEventListener](MediaCas.md))to receives scheme-specific notifications from a MediaCas instance.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEvent](../android/media/MediaCas.EventListener.md))`(`mediaCas:` ` [MediaCas](MediaCas.md)`, `event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Notify the listener of a scheme-specific event from the CA system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPluginStatusUpdate](../android/media/MediaCas.EventListener.md))`(`mediaCas:` ` [MediaCas](MediaCas.md)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify the listener that the cas plugin status is updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResourceLost](../android/media/MediaCas.EventListener.md))`(`mediaCas:` ` [MediaCas](MediaCas.md)`)` Notify the listener that the session resources was lost. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionEvent](../android/media/MediaCas.EventListener.md))`(`mediaCas:` ` [MediaCas](MediaCas.md)`, `session:` ` [MediaCas.Session](../android/media/MediaCas.Session.md)`, `event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Notify the listener of a scheme-specific session event from CA system. |

## Public methods

### onEvent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEvent(
    mediaCas: MediaCas, 
    event: Int, 
    arg: Int, 
    data: ByteArray?
): Unit
```

Notify the listener of a scheme-specific event from the CA system.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCas` | [MediaCas](MediaCas.md):the MediaCas object to receive this event. This value cannot be`null`. |
| `event` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer whose meaning is scheme-specific. |
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer whose meaning is scheme-specific. |
| --- | --- |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:a byte array of data whose format and meaning are scheme-specific. This value may be`null`. |

### onPluginStatusUpdate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPluginStatusUpdate(
    mediaCas: MediaCas, 
    status: Int, 
    arg: Int
): Unit
```

Notify the listener that the cas plugin status is updated.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCas` | [MediaCas](MediaCas.md):the MediaCas object to receive this event. This value cannot be`null`. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the plugin status which is updated. Value is [android.media.MediaCas#PLUGIN_STATUS_PHYSICAL_MODULE_CHANGED](MediaCas.md), or [android.media.MediaCas#PLUGIN_STATUS_SESSION_NUMBER_CHANGED](MediaCas.md) |
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer whose meaning is specific to the status to be updated. |
| --- | --- |

### onResourceLost

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onResourceLost(mediaCas: MediaCas): Unit
```

Notify the listener that the session resources was lost.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCas` | [MediaCas](MediaCas.md):the MediaCas object to receive this event. This value cannot be`null`. |

### onSessionEvent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSessionEvent(
    mediaCas: MediaCas, 
    session: MediaCas.Session, 
    event: Int, 
    arg: Int, 
    data: ByteArray?
): Unit
```

Notify the listener of a scheme-specific session event from CA system.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCas` | [MediaCas](MediaCas.md):the MediaCas object to receive this event. This value cannot be`null`. |
| `session` | [MediaCas.Session](../android/media/MediaCas.Session.md):session object which the event is for. This value cannot be`null`. |
| `event` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer whose meaning is scheme-specific. |
| --- | --- |
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer whose meaning is scheme-specific. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:a byte array of data whose format and meaning are scheme-specific. This value may be`null`. |
