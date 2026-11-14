# MediaCas.EventListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaCas.EventListener "View this page in Java") 
| --- | --- |

```
interface EventListener
```

| [android.media.MediaCas.EventListener](https://developer.android.com/reference/kotlin/android/media/MediaCas.EventListener#) |

An interface registered by the caller to [setEventListener](https://developer.android.com/reference/kotlin/android/media/MediaCas#setEventListener(android.media.MediaCas.EventListener,%20android.os.Handler))to receives scheme-specific notifications from a MediaCas instance.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEvent](https://developer.android.com/reference/kotlin/android/media/MediaCas.EventListener#onEvent(android.media.MediaCas,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray))`(`mediaCas:` ` [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas)`, `event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Notify the listener of a scheme-specific event from the CA system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPluginStatusUpdate](https://developer.android.com/reference/kotlin/android/media/MediaCas.EventListener#onPluginStatusUpdate(android.media.MediaCas,%20kotlin.Int,%20kotlin.Int))`(`mediaCas:` ` [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas)`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify the listener that the cas plugin status is updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResourceLost](https://developer.android.com/reference/kotlin/android/media/MediaCas.EventListener#onResourceLost(android.media.MediaCas))`(`mediaCas:` ` [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas)`)` Notify the listener that the session resources was lost. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionEvent](https://developer.android.com/reference/kotlin/android/media/MediaCas.EventListener#onSessionEvent(android.media.MediaCas,%20android.media.MediaCas.Session,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray))`(`mediaCas:` ` [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas)`, `session:` ` [MediaCas.Session](https://developer.android.com/reference/kotlin/android/media/MediaCas.Session)`, `event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `arg:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Notify the listener of a scheme-specific session event from CA system. |

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
| `mediaCas` | [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas):the MediaCas object to receive this event. This value cannot be`null`. |
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
| `mediaCas` | [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas):the MediaCas object to receive this event. This value cannot be`null`. |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the plugin status which is updated. Value is [android.media.MediaCas#PLUGIN_STATUS_PHYSICAL_MODULE_CHANGED](https://developer.android.com/reference/kotlin/android/media/MediaCas#PLUGIN_STATUS_PHYSICAL_MODULE_CHANGED:kotlin.Int), or [android.media.MediaCas#PLUGIN_STATUS_SESSION_NUMBER_CHANGED](https://developer.android.com/reference/kotlin/android/media/MediaCas#PLUGIN_STATUS_SESSION_NUMBER_CHANGED:kotlin.Int) |
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
| `mediaCas` | [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas):the MediaCas object to receive this event. This value cannot be`null`. |

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
| `mediaCas` | [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas):the MediaCas object to receive this event. This value cannot be`null`. |
| `session` | [MediaCas.Session](https://developer.android.com/reference/kotlin/android/media/MediaCas.Session):session object which the event is for. This value cannot be`null`. |
| `event` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer whose meaning is scheme-specific. |
| --- | --- |
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer whose meaning is scheme-specific. |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:a byte array of data whose format and meaning are scheme-specific. This value may be`null`. |
