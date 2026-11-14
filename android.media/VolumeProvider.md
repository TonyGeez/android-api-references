# VolumeProvider

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VolumeProvider

Kotlin| [Java](https://developer.android.com/reference/android/media/VolumeProvider "View this page in Java") 

```
abstract class VolumeProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.VolumeProvider](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#) |

Handles requests to adjust or set the volume on a session. This is also used to push volume updates back to the session. The provider must call [setCurrentVolume(int)](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#setCurrentVolume(kotlin.Int))each time the volume being provided changes.

You can set a volume provider on a session by calling [MediaSession.setPlaybackToRemote](https://developer.android.com/reference/kotlin/android/media/session/MediaSession#setPlaybackToRemote(android.media.VolumeProvider)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VOLUME_CONTROL_ABSOLUTE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_ABSOLUTE:kotlin.Int) The volume control uses an absolute value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VOLUME_CONTROL_FIXED](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_FIXED:kotlin.Int) The volume is fixed and can not be modified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VOLUME_CONTROL_RELATIVE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_RELATIVE:kotlin.Int) The volume control uses relative adjustment via [onAdjustVolume(int)](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#onAdjustVolume(kotlin.Int)). |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VolumeProvider](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VolumeProvider(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`volumeControl:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxVolume:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `currentVolume:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new volume provider for handling volume events. |
| [VolumeProvider](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VolumeProvider(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String))`(`volumeControl:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxVolume:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `currentVolume:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `volumeControlId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Creates a new volume provider for handling volume events. |

| Public methods ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentVolume](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#getCurrentVolume())`()` Gets the current volume. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxVolume](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#getMaxVolume())`()` Gets the maximum volume this provider allows. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVolumeControl](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#getVolumeControl())`()` Gets the volume control type that this volume provider uses. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getVolumeControlId](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#getVolumeControlId())`()` Gets the [routing controller id](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController#getId())of the [RoutingController](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController) associated with this volume provider, or null if unset. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdjustVolume](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#onAdjustVolume(kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Override to handle requests to adjust the volume of the current output. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetVolumeTo](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#onSetVolumeTo(kotlin.Int))`(`volume:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Override to handle requests to set the volume of the current output. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrentVolume](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#setCurrentVolume(kotlin.Int))`(`currentVolume:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notifies the system that the current volume has been changed. |

## Constants

### VOLUME_CONTROL_ABSOLUTE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VOLUME_CONTROL_ABSOLUTE: Int
```

The volume control uses an absolute value. It may be adjusted using [onAdjustVolume(int)](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#onAdjustVolume(kotlin.Int))or set directly using [onSetVolumeTo(int)](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#onSetVolumeTo(kotlin.Int)). 

 Value: 2

### VOLUME_CONTROL_FIXED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VOLUME_CONTROL_FIXED: Int
```

The volume is fixed and can not be modified. Requests to change volume should be ignored. 

 Value: 0

### VOLUME_CONTROL_RELATIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VOLUME_CONTROL_RELATIVE: Int
```

The volume control uses relative adjustment via [onAdjustVolume(int)](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#onAdjustVolume(kotlin.Int)). Attempts to set the volume to a specific value should be ignored. 

 Value: 1

## Public constructors

### VolumeProvider

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VolumeProvider(
    volumeControl: Int, 
    maxVolume: Int, 
    currentVolume: Int)
```

Creates a new volume provider for handling volume events.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `volumeControl` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):See [getVolumeControl()](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#getVolumeControl()). Value is [android.media.VolumeProvider#VOLUME_CONTROL_FIXED](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_FIXED:kotlin.Int), [android.media.VolumeProvider#VOLUME_CONTROL_RELATIVE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_RELATIVE:kotlin.Int), or [android.media.VolumeProvider#VOLUME_CONTROL_ABSOLUTE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_ABSOLUTE:kotlin.Int) |
| `maxVolume` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum allowed volume. |
| `currentVolume` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current volume on the output. |

### VolumeProvider

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VolumeProvider(
    volumeControl: Int, 
    maxVolume: Int, 
    currentVolume: Int, 
    volumeControlId: String?)
```

Creates a new volume provider for handling volume events.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `volumeControl` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):See [getVolumeControl()](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#getVolumeControl()). Value is [android.media.VolumeProvider#VOLUME_CONTROL_FIXED](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_FIXED:kotlin.Int), [android.media.VolumeProvider#VOLUME_CONTROL_RELATIVE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_RELATIVE:kotlin.Int), or [android.media.VolumeProvider#VOLUME_CONTROL_ABSOLUTE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_ABSOLUTE:kotlin.Int) |
| `maxVolume` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum allowed volume. |
| `currentVolume` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current volume on the output. |
| `volumeControlId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:See [getVolumeControlId()](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#getVolumeControlId()). This value may be`null`. |

## Public methods

### getCurrentVolume

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrentVolume(): Int
```

Gets the current volume. This will be the last value set by [setCurrentVolume(int)](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#setCurrentVolume(kotlin.Int)).

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The current volume. |

### getMaxVolume

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxVolume(): Int
```

Gets the maximum volume this provider allows.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The max allowed volume. |

### getVolumeControl

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeControl(): Int
```

Gets the volume control type that this volume provider uses.

One of [VOLUME_CONTROL_FIXED](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_FIXED:kotlin.Int), [VOLUME_CONTROL_ABSOLUTE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_ABSOLUTE:kotlin.Int), or [VOLUME_CONTROL_RELATIVE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_RELATIVE:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The volume control type for this volume provider Value is [android.media.VolumeProvider#VOLUME_CONTROL_FIXED](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_FIXED:kotlin.Int), [android.media.VolumeProvider#VOLUME_CONTROL_RELATIVE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_RELATIVE:kotlin.Int), or [android.media.VolumeProvider#VOLUME_CONTROL_ABSOLUTE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#VOLUME_CONTROL_ABSOLUTE:kotlin.Int) |

### getVolumeControlId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolumeControlId(): String?
```

Gets the [routing controller id](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController#getId())of the [RoutingController](https://developer.android.com/reference/kotlin/android/media/MediaRouter2.RoutingController) associated with this volume provider, or null if unset.

This id allows mapping this volume provider to a routing controller, which provides information about the media route and allows controlling its volume. 

### onAdjustVolume

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAdjustVolume(direction: Int): Unit
```

Override to handle requests to adjust the volume of the current output. Direction will be one of [AudioManager.ADJUST_LOWER](https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_LOWER:kotlin.Int), [AudioManager.ADJUST_RAISE](https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_RAISE:kotlin.Int), [AudioManager.ADJUST_SAME](https://developer.android.com/reference/kotlin/android/media/AudioManager#ADJUST_SAME:kotlin.Int). After the volume has been modified [setCurrentVolume](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#setCurrentVolume(kotlin.Int))must be called to notify the system.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The direction to change the volume in. |

### onSetVolumeTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSetVolumeTo(volume: Int): Unit
```

Override to handle requests to set the volume of the current output. After the volume has been modified [setCurrentVolume](https://developer.android.com/reference/kotlin/android/media/VolumeProvider#setCurrentVolume(kotlin.Int))must be called to notify the system.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `volume` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The volume to set the output to. |

### setCurrentVolume

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCurrentVolume(currentVolume: Int): Unit
```

Notifies the system that the current volume has been changed. This must be called every time the volume changes to ensure it is displayed properly.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------|
| `currentVolume` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current volume on the output. |
