# VolumeAutomation

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VolumeAutomation

Kotlin| [Java](../android/media/VolumeAutomation.md) 
| --- | --- |

```
interface VolumeAutomation
```

| [android.media.VolumeAutomation](../android/media/VolumeAutomation.md) |

| Known Direct Subclasses [AudioTrack](../android/media/AudioTrack.md), [MediaPlayer](../android/media/MediaPlayer.md) |-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------| | [AudioTrack](../android/media/AudioTrack.md) | The AudioTrack class manages and plays a single audio resource for Java applications. | | [MediaPlayer](../android/media/MediaPlayer.md) | MediaPlayer class can be used to control playback of audio/video files and streams. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

`VolumeAutomation`defines an interface for automatic volume control of [AudioTrack](../android/media/AudioTrack.md) and [MediaPlayer](../android/media/MediaPlayer.md) objects.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [VolumeShaper](../android/media/VolumeShaper.md) | [createVolumeShaper](../android/media/VolumeAutomation.md))`(`configuration:` ` [VolumeShaper.Configuration](../android/media/VolumeShaper.Configuration.md)`)` Returns a [VolumeShaper](../android/media/VolumeShaper.md) object that can be used modify the volume envelope of the player or track. |

## Public methods

### createVolumeShaper

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createVolumeShaper(configuration: VolumeShaper.Configuration): VolumeShaper
```

Returns a [VolumeShaper](../android/media/VolumeShaper.md) object that can be used modify the volume envelope of the player or track.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configuration` | [VolumeShaper.Configuration](../android/media/VolumeShaper.Configuration.md):the [configuration](../android/media/VolumeShaper.Configuration.md) that specifies the curve and duration to use. This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------|
| [VolumeShaper](../android/media/VolumeShaper.md) | a`VolumeShaper`object This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`configuration`is not allowed by the player. |
| `java.lang.IllegalStateException` | if too many`VolumeShaper`s are requested or the state of the player does not permit its creation (e.g. player is released). |
