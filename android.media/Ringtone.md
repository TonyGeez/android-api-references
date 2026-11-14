# Ringtone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Ringtone

Kotlin| [Java](Ringtone.md) 
| --- | --- |

```
open class Ringtone
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.Ringtone](Ringtone.md) |

Ringtone provides a quick method for playing a ringtone, notification, or other similar types of sounds.

For ways of retrieving [Ringtone](Ringtone.md) objects or to show a ringtone picker, see [RingtoneManager](RingtoneManager.md).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AudioAttributes](AudioAttributes.md)! | [getAudioAttributes](Ringtone.md))`()` Returns the [AudioAttributes](AudioAttributes.md) used by this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStreamType](Ringtone.md))`()` Gets the stream type where this ringtone will be played. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTitle](Ringtone.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Returns a human-presentable title for ringtone. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVolume](Ringtone.md))`()` Returns the volume scalar set on this player. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHapticGeneratorEnabled](Ringtone.md))`()` Return whether the [android.media.audiofx.HapticGenerator](../android.media.audiofx/HapticGenerator.md) effect is enabled or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLooping](Ringtone.md))`()` Returns whether the looping mode was enabled on this player. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPlaying](Ringtone.md))`()` Whether this ringtone is currently playing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [play](Ringtone.md))`()` Plays the ringtone. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioAttributes](Ringtone.md))`(`attributes:` ` [AudioAttributes](AudioAttributes.md)!`)` Sets the [AudioAttributes](AudioAttributes.md) for this ringtone. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setHapticGeneratorEnabled](Ringtone.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable the [android.media.audiofx.HapticGenerator](../android.media.audiofx/HapticGenerator.md) effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLooping](Ringtone.md))`(`looping:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the player to be looping or non-looping. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStreamType](Ringtone.md))`(`streamType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the stream type where this ringtone will be played. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolume](Ringtone.md))`(`volume:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the volume on this player. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](Ringtone.md))`()` Stops a playing ringtone. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](Ringtone.md))`()` <br /> |

## Public methods

### getAudioAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAudioAttributes(): AudioAttributes!
```

Returns the [AudioAttributes](AudioAttributes.md) used by this object.

| Return ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AudioAttributes](AudioAttributes.md)! | the [AudioAttributes](AudioAttributes.md) that were set with [setAudioAttributes(android.media.AudioAttributes)](Ringtone.md))or the default attributes if none were set. |

### getStreamType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStreamType(): Int
```

**Deprecated:** *use of stream types is deprecated, see [setAudioAttributes(android.media.AudioAttributes)](Ringtone.md))*

Gets the stream type where this ringtone will be played.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The stream type, see [AudioManager](AudioManager.md). |

### getTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTitle(context: Context!): String!
```

Returns a human-presentable title for ringtone. Looks in media content provider. If not in either, uses the filename

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:A context used for querying. |

### getVolume

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVolume(): Float
```

Returns the volume scalar set on this player.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a value between 0.0f and 1.0f. |

### isHapticGeneratorEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isHapticGeneratorEnabled(): Boolean
```

Return whether the [android.media.audiofx.HapticGenerator](../android.media.audiofx/HapticGenerator.md) effect is enabled or not.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the HapticGenerator is enabled. |

### isLooping

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLooping(): Boolean
```

Returns whether the looping mode was enabled on this player.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this player loops when playing. |

### isPlaying

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPlaying(): Boolean
```

Whether this ringtone is currently playing.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if playing, false otherwise. |

### play

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun play(): Unit
```

Plays the ringtone. 

### setAudioAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAudioAttributes(attributes: AudioAttributes!): Unit
```

Sets the [AudioAttributes](AudioAttributes.md) for this ringtone.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [AudioAttributes](AudioAttributes.md)!:the non-null attributes characterizing this ringtone. |

### setHapticGeneratorEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHapticGeneratorEnabled(enabled: Boolean): Boolean
```

Enable or disable the [android.media.audiofx.HapticGenerator](../android.media.audiofx/HapticGenerator.md) effect. The effect can only be enabled on devices that support the effect.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the HapticGenerator effect is successfully enabled. Otherwise, return false. |

**See Also**

- [android.media.audiofx.HapticGenerator#isAvailable()](../android.media.audiofx/HapticGenerator.md)) 

### setLooping

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLooping(looping: Boolean): Unit
```

Sets the player to be looping or non-looping.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `looping` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to loop or not. |

### setStreamType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStreamType(streamType: Int): Unit
```

**Deprecated:** *use [setAudioAttributes(android.media.AudioAttributes)](Ringtone.md))*

Sets the stream type where this ringtone will be played.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The stream, see [AudioManager](AudioManager.md). |

### setVolume

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVolume(volume: Float): Unit
```

Sets the volume on this player.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `volume` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):a raw scalar in range 0.0 to 1.0, where 0.0 mutes this player, and 1.0 corresponds to no attenuation being applied. |

### stop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stop(): Unit
```

Stops a playing ringtone.

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
