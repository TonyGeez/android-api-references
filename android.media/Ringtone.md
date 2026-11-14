# Ringtone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Ringtone

Kotlin| [Java](https://developer.android.com/reference/android/media/Ringtone "View this page in Java") 
| --- | --- |

```
open class Ringtone
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.Ringtone](https://developer.android.com/reference/kotlin/android/media/Ringtone#) |

Ringtone provides a quick method for playing a ringtone, notification, or other similar types of sounds.

For ways of retrieving [Ringtone](https://developer.android.com/reference/kotlin/android/media/Ringtone#) objects or to show a ringtone picker, see [RingtoneManager](https://developer.android.com/reference/kotlin/android/media/RingtoneManager).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes)! | [getAudioAttributes](https://developer.android.com/reference/kotlin/android/media/Ringtone#getAudioAttributes())`()` Returns the [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes) used by this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStreamType](https://developer.android.com/reference/kotlin/android/media/Ringtone#getStreamType())`()` Gets the stream type where this ringtone will be played. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTitle](https://developer.android.com/reference/kotlin/android/media/Ringtone#getTitle(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Returns a human-presentable title for ringtone. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getVolume](https://developer.android.com/reference/kotlin/android/media/Ringtone#getVolume())`()` Returns the volume scalar set on this player. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHapticGeneratorEnabled](https://developer.android.com/reference/kotlin/android/media/Ringtone#isHapticGeneratorEnabled())`()` Return whether the [android.media.audiofx.HapticGenerator](https://developer.android.com/reference/kotlin/android/media/audiofx/HapticGenerator) effect is enabled or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLooping](https://developer.android.com/reference/kotlin/android/media/Ringtone#isLooping())`()` Returns whether the looping mode was enabled on this player. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPlaying](https://developer.android.com/reference/kotlin/android/media/Ringtone#isPlaying())`()` Whether this ringtone is currently playing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [play](https://developer.android.com/reference/kotlin/android/media/Ringtone#play())`()` Plays the ringtone. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAudioAttributes](https://developer.android.com/reference/kotlin/android/media/Ringtone#setAudioAttributes(android.media.AudioAttributes))`(`attributes:` ` [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes)!`)` Sets the [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes) for this ringtone. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setHapticGeneratorEnabled](https://developer.android.com/reference/kotlin/android/media/Ringtone#setHapticGeneratorEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable the [android.media.audiofx.HapticGenerator](https://developer.android.com/reference/kotlin/android/media/audiofx/HapticGenerator) effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLooping](https://developer.android.com/reference/kotlin/android/media/Ringtone#setLooping(kotlin.Boolean))`(`looping:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the player to be looping or non-looping. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStreamType](https://developer.android.com/reference/kotlin/android/media/Ringtone#setStreamType(kotlin.Int))`(`streamType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the stream type where this ringtone will be played. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolume](https://developer.android.com/reference/kotlin/android/media/Ringtone#setVolume(kotlin.Float))`(`volume:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the volume on this player. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/android/media/Ringtone#stop())`()` Stops a playing ringtone. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/Ringtone#finalize())`()` <br /> |

## Public methods

### getAudioAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAudioAttributes(): AudioAttributes!
```

Returns the [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes) used by this object.

| Return ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes)! | the [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes) that were set with [setAudioAttributes(android.media.AudioAttributes)](https://developer.android.com/reference/kotlin/android/media/Ringtone#setAudioAttributes(android.media.AudioAttributes))or the default attributes if none were set. |

### getStreamType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStreamType(): Int
```

**Deprecated:** *use of stream types is deprecated, see [setAudioAttributes(android.media.AudioAttributes)](https://developer.android.com/reference/kotlin/android/media/Ringtone#setAudioAttributes(android.media.AudioAttributes))*

Gets the stream type where this ringtone will be played.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The stream type, see [AudioManager](https://developer.android.com/reference/kotlin/android/media/AudioManager). |

### getTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTitle(context: Context!): String!
```

Returns a human-presentable title for ringtone. Looks in media content provider. If not in either, uses the filename

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:A context used for querying. |

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

Return whether the [android.media.audiofx.HapticGenerator](https://developer.android.com/reference/kotlin/android/media/audiofx/HapticGenerator) effect is enabled or not.

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

Sets the [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes) for this ringtone.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes)!:the non-null attributes characterizing this ringtone. |

### setHapticGeneratorEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHapticGeneratorEnabled(enabled: Boolean): Boolean
```

Enable or disable the [android.media.audiofx.HapticGenerator](https://developer.android.com/reference/kotlin/android/media/audiofx/HapticGenerator) effect. The effect can only be enabled on devices that support the effect.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the HapticGenerator effect is successfully enabled. Otherwise, return false. |

**See Also**

- [android.media.audiofx.HapticGenerator#isAvailable()](https://developer.android.com/reference/kotlin/android/media/audiofx/HapticGenerator#isAvailable()) 

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

**Deprecated:** *use [setAudioAttributes(android.media.AudioAttributes)](https://developer.android.com/reference/kotlin/android/media/Ringtone#setAudioAttributes(android.media.AudioAttributes))*

Sets the stream type where this ringtone will be played.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `streamType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The stream, see [AudioManager](https://developer.android.com/reference/kotlin/android/media/AudioManager). |

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
