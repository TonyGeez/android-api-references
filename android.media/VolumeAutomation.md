# VolumeAutomation

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VolumeAutomation

Kotlin| [Java](https://developer.android.com/reference/android/media/VolumeAutomation "View this page in Java") 

```
interface VolumeAutomation
```

| [android.media.VolumeAutomation](https://developer.android.com/reference/kotlin/android/media/VolumeAutomation#) |

| Known Direct Subclasses [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack), [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer) |-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------| | [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack) | The AudioTrack class manages and plays a single audio resource for Java applications. | | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer) | MediaPlayer class can be used to control playback of audio/video files and streams. | |

`VolumeAutomation`defines an interface for automatic volume control of [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack) and [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer) objects.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [VolumeShaper](https://developer.android.com/reference/kotlin/android/media/VolumeShaper) | [createVolumeShaper](https://developer.android.com/reference/kotlin/android/media/VolumeAutomation#createVolumeShaper(android.media.VolumeShaper.Configuration))`(`configuration:` ` [VolumeShaper.Configuration](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Configuration)`)` Returns a [VolumeShaper](https://developer.android.com/reference/kotlin/android/media/VolumeShaper) object that can be used modify the volume envelope of the player or track. |

## Public methods

### createVolumeShaper

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createVolumeShaper(configuration: VolumeShaper.Configuration): VolumeShaper
```

Returns a [VolumeShaper](https://developer.android.com/reference/kotlin/android/media/VolumeShaper) object that can be used modify the volume envelope of the player or track.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configuration` | [VolumeShaper.Configuration](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Configuration):the [configuration](https://developer.android.com/reference/kotlin/android/media/VolumeShaper.Configuration) that specifies the curve and duration to use. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------|
| [VolumeShaper](https://developer.android.com/reference/kotlin/android/media/VolumeShaper) | a`VolumeShaper`object This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`configuration`is not allowed by the player. |
| `java.lang.IllegalStateException` | if too many`VolumeShaper`s are requested or the state of the player does not permit its creation (e.g. player is released). |
