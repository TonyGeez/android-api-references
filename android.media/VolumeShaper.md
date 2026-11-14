# VolumeShaper

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VolumeShaper

Kotlin| [Java](https://developer.android.com/reference/android/media/VolumeShaper "View this page in Java") 

```
class VolumeShaper : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.VolumeShaper](https://developer.android.com/reference/kotlin/android/media/VolumeShaper#) |

The`VolumeShaper`class is used to automatically control audio volume during media playback, allowing simple implementation of transition effects and ducking. It is created from implementations of`VolumeAutomation`, such as`MediaPlayer`and`AudioTrack`(referred to as "players" below), by [MediaPlayer.createVolumeShaper](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#createVolumeShaper(android.media.VolumeShaper.Configuration))or [AudioTrack.createVolumeShaper](https://developer.android.com/reference/kotlin/android/media/AudioTrack#createVolumeShaper(android.media.VolumeShaper.Configuration)). A`VolumeShaper`is intended for short volume changes. If the audio output sink changes during a`VolumeShaper`transition, the precise curve position may be lost, and the`VolumeShaper`may advance to the end of the curve for the new audio output sink. The`VolumeShaper`appears as an additional scaling on the audio output, and adjusts independently of track or stream volume controls.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Configuration](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Configuration) The`VolumeShaper.Configuration`class contains curve and duration information. |
| | [Operation](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation) The`VolumeShaper.Operation`class is used to specify operations to the`VolumeShaper`that affect the volume change. |

| Public methods ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [apply](https://developer.android.com/reference/kotlin/android/media/VolumeShaper#apply(android.media.VolumeShaper.Operation))`(`operation:` ` [VolumeShaper.Operation](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation)`)` Applies the [VolumeShaper.Operation](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation) to the`VolumeShaper`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/media/VolumeShaper#close())`()` Releases the`VolumeShaper`object; any volume scale due to the`VolumeShaper`is removed after closing. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVolume](https://developer.android.com/reference/kotlin/android/media/VolumeShaper#getVolume())`()` Returns the current volume scale attributable to the`VolumeShaper`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [replace](https://developer.android.com/reference/kotlin/android/media/VolumeShaper#replace(android.media.VolumeShaper.Configuration,%20android.media.VolumeShaper.Operation,%20kotlin.Boolean))`(`configuration:` ` [VolumeShaper.Configuration](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Configuration)`, `operation:` ` [VolumeShaper.Operation](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation)`, `join:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Replaces the current`VolumeShaper``configuration`with a new`configuration`. |

| Protected methods ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/VolumeShaper#finalize())`()` <br /> |

## Public methods

### apply

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun apply(operation: VolumeShaper.Operation): Unit
```

Applies the [VolumeShaper.Operation](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation) to the`VolumeShaper`. Applying [VolumeShaper.Operation.PLAY](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation#PLAY:android.media.VolumeShaper.Operation) after`PLAY`or [VolumeShaper.Operation.REVERSE](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation#REVERSE:android.media.VolumeShaper.Operation) after`REVERSE`has no effect. Applying [VolumeShaper.Operation.PLAY](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation#PLAY:android.media.VolumeShaper.Operation) when the player hasn't started will synchronously start the`VolumeShaper`when playback begins.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `operation` | [VolumeShaper.Operation](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation):the`operation`to apply. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the player is uninitialized or if there is a critical failure. In that case, the`VolumeShaper`should be recreated. |

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Releases the`VolumeShaper`object; any volume scale due to the`VolumeShaper`is removed after closing. If the volume does not reach 1.f when the`VolumeShaper`is closed (or finalized), there may be an abrupt change of volume.`close()`may be safely called after a prior`close()`. This class implements the Java`AutoClosable`interface and may be used with try-with-resources.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### getVolume

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolume(): Float
```

Returns the current volume scale attributable to the`VolumeShaper`. This is the last volume from the`VolumeShaper`used for the player, or the initial volume if the`VolumeShaper`hasn't been started with [VolumeShaper.Operation.PLAY](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation#PLAY:android.media.VolumeShaper.Operation).

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the volume, linearly represented as a value between 0.f and 1.f. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the player is uninitialized or if there is a critical failure. In that case, the`VolumeShaper`should be recreated. |

### replace

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun replace(
    configuration: VolumeShaper.Configuration, 
    operation: VolumeShaper.Operation, 
    join: Boolean
): Unit
```

Replaces the current`VolumeShaper``configuration`with a new`configuration`. This allows the user to change the volume shape while the existing`VolumeShaper`is in effect. The effect of`replace()`is similar to an atomic close of the existing`VolumeShaper`and creation of a new`VolumeShaper`. If the`operation`is [VolumeShaper.Operation.PLAY](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation#PLAY:android.media.VolumeShaper.Operation) then the new curve starts immediately. If the`operation`is [VolumeShaper.Operation.REVERSE](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation#REVERSE:android.media.VolumeShaper.Operation), then the new curve will be delayed until`PLAY`is applied.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configuration` | [VolumeShaper.Configuration](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Configuration):the new`configuration`to use. This value cannot be`null`. |
| `operation` | [VolumeShaper.Operation](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Operation):the`operation`to apply to the`VolumeShaper`This value cannot be`null`. |
| `join` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, match the start volume of the new`configuration`to the current volume of the existing`VolumeShaper`, to avoid discontinuity. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the player is uninitialized or if there is a critical failure. In that case, the`VolumeShaper`should be recreated. |

## Protected methods

### finalize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
