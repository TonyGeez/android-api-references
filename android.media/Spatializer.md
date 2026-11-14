Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Spatializer

Kotlin | [Java](https://developer.android.com/reference/android/media/Spatializer "View this page in Java")
| --- | --- |

```
open class Spatializer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.Spatializer](https://developer.android.com/reference/kotlin/android/media/Spatializer#) |

Spatializer provides access to querying capabilities and behavior of sound spatialization on the device. Sound spatialization simulates sounds originating around the listener as if they were coming from virtual speakers placed around the listener. 
Support for spatialization is optional, use `https://developer.android.com/reference/kotlin/android/media/AudioManager#getSpatializer()` to obtain an instance of this class if the feature is supported.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/Spatializer.OnHeadTrackerAvailableListener` Interface to be notified of changes to the availability of a head tracker on the audio device to be used by the spatializer effect. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/Spatializer.OnSpatializerStateChangedListener` An interface to be notified of changes to the state of the spatializer effect. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#SPATIALIZER_IMMERSIVE_LEVEL_MULTICHANNEL:kotlin.Int` Constant indicating the `Spatializer` on this device supports multichannel spatialization. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#SPATIALIZER_IMMERSIVE_LEVEL_NONE:kotlin.Int` Constant indicating there are no spatialization capabilities supported on this device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#SPATIALIZER_IMMERSIVE_LEVEL_OTHER:kotlin.Int` Constant indicating the `Spatializer` on this device supports a spatialization mode that differs from the ones available at this SDK level. |
| --- | --- |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#addOnHeadTrackerAvailableListener(java.util.concurrent.Executor,%20android.media.Spatializer.OnHeadTrackerAvailableListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/media/Spatializer.OnHeadTrackerAvailableListener)` Adds a listener to be notified of changes to the availability of a head tracker. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#addOnSpatializerStateChangedListener(java.util.concurrent.Executor,%20android.media.Spatializer.OnSpatializerStateChangedListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/media/Spatializer.OnSpatializerStateChangedListener)` Adds a listener to be notified of changes to the enabled state of the `Spatializer`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#canBeSpatialized(android.media.AudioAttributes,%20android.media.AudioFormat)(attributes: https://developer.android.com/reference/kotlin/android/media/AudioAttributes, format: https://developer.android.com/reference/kotlin/android/media/AudioFormat)` Returns whether audio of the given `https://developer.android.com/reference/kotlin/android/media/AudioFormat`, played with the given `https://developer.android.com/reference/kotlin/android/media/AudioAttributes` can be spatialized. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#getImmersiveAudioLevel()()` Return the level of support for the spatialization feature on this device. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/media/Spatializer#getSpatializedChannelMasks()()` Returns a list of channel masks that represent the widest channel masks the spatializer is capable of rendering with individual channel positions. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#isAvailable()()` Returns whether spatialization is available. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#isEnabled()()` Returns whether spatialization is enabled or not. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#isHeadTrackerAvailable()()` Returns whether a head tracker is currently available for the audio device used by the spatializer effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#removeOnHeadTrackerAvailableListener(android.media.Spatializer.OnHeadTrackerAvailableListener)(listener: https://developer.android.com/reference/kotlin/android/media/Spatializer.OnHeadTrackerAvailableListener)` Removes a previously registered listener for the availability of a head tracker. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/Spatializer#removeOnSpatializerStateChangedListener(android.media.Spatializer.OnSpatializerStateChangedListener)(listener: https://developer.android.com/reference/kotlin/android/media/Spatializer.OnSpatializerStateChangedListener)` Removes a previously added listener for changes to the enabled state of the `Spatializer`. |

## Constants

### SPATIALIZER_IMMERSIVE_LEVEL_MULTICHANNEL

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SPATIALIZER_IMMERSIVE_LEVEL_MULTICHANNEL: Int
```

Constant indicating the `Spatializer` on this device supports multichannel spatialization.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer#getImmersiveAudioLevel()`

### SPATIALIZER_IMMERSIVE_LEVEL_NONE

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SPATIALIZER_IMMERSIVE_LEVEL_NONE: Int
```

Constant indicating there are no spatialization capabilities supported on this device.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer#getImmersiveAudioLevel()`

### SPATIALIZER_IMMERSIVE_LEVEL_OTHER

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SPATIALIZER_IMMERSIVE_LEVEL_OTHER: Int
```

Constant indicating the `Spatializer` on this device supports a spatialization mode that differs from the ones available at this SDK level.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer#getImmersiveAudioLevel()`

## Public methods

### addOnHeadTrackerAvailableListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnHeadTrackerAvailableListener(
    executor: Executor, 
    listener: Spatializer.OnHeadTrackerAvailableListener
): Unit
```

Adds a listener to be notified of changes to the availability of a head tracker.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the `Executor` handling the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [Spatializer.OnHeadTrackerAvailableListener](https://developer.android.com/reference/kotlin/android/media/Spatializer.OnHeadTrackerAvailableListener): the listener to receive availability updates. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer#removeOnHeadTrackerAvailableListener(android.media.Spatializer.OnHeadTrackerAvailableListener)`

### addOnSpatializerStateChangedListener

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnSpatializerStateChangedListener(
    executor: Executor, 
    listener: Spatializer.OnSpatializerStateChangedListener
): Unit
```

Adds a listener to be notified of changes to the enabled state of the `Spatializer`.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): the `Executor` handling the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [Spatializer.OnSpatializerStateChangedListener](https://developer.android.com/reference/kotlin/android/media/Spatializer.OnSpatializerStateChangedListener): the listener to receive enabled state updates. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer#isEnabled()`

### canBeSpatialized

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canBeSpatialized(
    attributes: AudioAttributes, 
    format: AudioFormat
): Boolean
```

Returns whether audio of the given `https://developer.android.com/reference/kotlin/android/media/AudioFormat`, played with the given `https://developer.android.com/reference/kotlin/android/media/AudioAttributes` can be spatialized. Note that the result reflects the capabilities of the device and may change when audio accessories are connected/disconnected (e.g. wired headphones plugged in or not). The result is independent from whether spatialization processing is enabled or not.

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes): the `AudioAttributes` of the content as used for playback. This value cannot be `null`. |
| `format` | [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat): the `AudioFormat` of the content as used for playback. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the device is capable of spatializing the combination of audio format and attributes, `false` otherwise. |

### getImmersiveAudioLevel

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getImmersiveAudioLevel(): Int
```

Return the level of support for the spatialization feature on this device. This level of support is independent of whether the `Spatializer` is currently enabled or available and will not change over time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the level of spatialization support. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/Spatializer#SPATIALIZER_IMMERSIVE_LEVEL_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/Spatializer#SPATIALIZER_IMMERSIVE_LEVEL_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/Spatializer#SPATIALIZER_IMMERSIVE_LEVEL_MULTICHANNEL:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer#isEnabled()`
- `https://developer.android.com/reference/kotlin/android/media/Spatializer#isAvailable()`

### getSpatializedChannelMasks

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSpatializedChannelMasks(): MutableList<Int!>
```

Returns a list of channel masks that represent the widest channel masks the spatializer is capable of rendering with individual channel positions. For instance a spatializer may only support virtual speaker positions for 5.1, it would therefore return `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_5POINT1:kotlin.Int`. But it would still return `true` when querying `https://developer.android.com/reference/kotlin/android/media/Spatializer#canBeSpatialized(android.media.AudioAttributes,%20android.media.AudioFormat)` it with a channel mask of `https://developer.android.com/reference/kotlin/android/media/AudioFormat#CHANNEL_OUT_7POINT1POINT2:kotlin.Int`: the sound present in each channel would still be heard, but the sounds from the rear, side and top pairs would be mixed together, and be spatialized at the same location.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | a list of channel masks following the `CHANNEL_OUT_*` output channel definitions found in `https://developer.android.com/reference/kotlin/android/media/AudioFormat`. This value cannot be `null`. |

### isAvailable

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAvailable(): Boolean
```

Returns whether spatialization is available. Reasons for spatialization being unavailable include situations where audio output is incompatible with sound spatialization, such as playback on a monophonic speaker. 
Note that spatialization can be available, but disabled by the user, in which case this method would still return `true`, whereas `https://developer.android.com/reference/kotlin/android/media/Spatializer#isEnabled()` would return `false`. 
Also when the feature is not supported on the device (indicated by `https://developer.android.com/reference/kotlin/android/media/Spatializer#getImmersiveAudioLevel()` returning `https://developer.android.com/reference/kotlin/android/media/Spatializer#SPATIALIZER_IMMERSIVE_LEVEL_NONE:kotlin.Int`), the return value will be false.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the spatializer effect is available and capable of processing the audio for the current configuration of the device, `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer#isEnabled()`

### isEnabled

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEnabled(): Boolean
```

Returns whether spatialization is enabled or not. A false value can originate for instance from the user electing to disable the feature, or when the feature is not supported on the device (indicated by `https://developer.android.com/reference/kotlin/android/media/Spatializer#getImmersiveAudioLevel()` returning `https://developer.android.com/reference/kotlin/android/media/Spatializer#SPATIALIZER_IMMERSIVE_LEVEL_NONE:kotlin.Int`). 
Note that this state reflects a platform-wide state of the "desire" to use spatialization, but availability of the audio processing is still dictated by the compatibility between the effect and the hardware configuration, as indicated by `https://developer.android.com/reference/kotlin/android/media/Spatializer#isAvailable()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if spatialization is enabled |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer#isAvailable()`

### isHeadTrackerAvailable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHeadTrackerAvailable(): Boolean
```

Returns whether a head tracker is currently available for the audio device used by the spatializer effect.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a head tracker is available and the effect is enabled, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer.OnHeadTrackerAvailableListener`
- `https://developer.android.com/reference/kotlin/android/media/Spatializer#addOnHeadTrackerAvailableListener(java.util.concurrent.Executor,%20android.media.Spatializer.OnHeadTrackerAvailableListener)`

### removeOnHeadTrackerAvailableListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnHeadTrackerAvailableListener(listener: Spatializer.OnHeadTrackerAvailableListener): Unit
```

Removes a previously registered listener for the availability of a head tracker.

| Parameters ||
|---|---|
| `listener` | [Spatializer.OnHeadTrackerAvailableListener](https://developer.android.com/reference/kotlin/android/media/Spatializer.OnHeadTrackerAvailableListener): the listener previously registered with `https://developer.android.com/reference/kotlin/android/media/Spatializer#addOnHeadTrackerAvailableListener(java.util.concurrent.Executor,%20android.media.Spatializer.OnHeadTrackerAvailableListener)` This value cannot be `null`. |

### removeOnSpatializerStateChangedListener

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnSpatializerStateChangedListener(listener: Spatializer.OnSpatializerStateChangedListener): Unit
```

Removes a previously added listener for changes to the enabled state of the `Spatializer`.

| Parameters ||
|---|---|
| `listener` | [Spatializer.OnSpatializerStateChangedListener](https://developer.android.com/reference/kotlin/android/media/Spatializer.OnSpatializerStateChangedListener): the listener to receive enabled state updates. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/Spatializer#isEnabled()`
