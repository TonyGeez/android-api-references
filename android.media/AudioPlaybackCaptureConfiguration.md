# AudioPlaybackCaptureConfiguration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioPlaybackCaptureConfiguration

Kotlin| [Java](../android/media/AudioPlaybackCaptureConfiguration.md) 
| --- | --- |

```
class AudioPlaybackCaptureConfiguration
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioPlaybackCaptureConfiguration](../android/media/AudioPlaybackCaptureConfiguration.md) |

Configuration for capturing audio played by other apps. When capturing audio signals played by other apps (and yours), you will only capture a mix of the audio signals played by players (such as AudioTrack or MediaPlayer) which present the following characteristics:

- the usage value MUST be [AudioAttributes.USAGE_UNKNOWN](../android/media/AudioAttributes.md) or [AudioAttributes.USAGE_GAME](../android/media/AudioAttributes.md) or [AudioAttributes.USAGE_MEDIA](../android/media/AudioAttributes.md). All other usages CAN NOT be captured.
- AND the capture policy set by their app (with [AudioManager.setAllowedCapturePolicy](../android/media/AudioManager.md))) or on each player (with [AudioAttributes.Builder.setAllowedCapturePolicy](../android/media/AudioAttributes.Builder.md))) is [AudioAttributes.ALLOW_CAPTURE_BY_ALL](../android/media/AudioAttributes.md), whichever is the most strict.
- AND their app attribute allowAudioPlaybackCapture in their manifest MUST either be:
 - set to "true"
 - not set, and their`targetSdkVersion`MUST be equal to or greater than [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md). Ie. Apps that do not target at least Android Q must explicitly opt-in to be captured by a MediaProjection.
- AND their apps MUST be in the same user profile as your app (eg work profile cannot capture user profile apps and vice-versa).

<br />

An example for creating a capture configuration for capturing all media playback: 

```kotlin
MediaProjection mediaProjection;
      // Retrieve a audio capable projection from the MediaProjectionManager
      AudioPlaybackCaptureConfiguration config =
          new AudioPlaybackCaptureConfiguration.Builder(mediaProjection)
          .addMatchingUsage(AudioAttributes.USAGE_MEDIA)
          .build();
      AudioRecord record = new AudioRecord.Builder()
          .setAudioPlaybackCaptureConfig(config)
          .build();
  
```

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/media/AudioPlaybackCaptureConfiguration.Builder.md) Builder for creating [AudioPlaybackCaptureConfiguration](../android/media/AudioPlaybackCaptureConfiguration.md) instances. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getExcludeUids](../android/media/AudioPlaybackCaptureConfiguration.md))`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getExcludeUsages](../android/media/AudioPlaybackCaptureConfiguration.md))`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getMatchingUids](../android/media/AudioPlaybackCaptureConfiguration.md))`()` <br /> |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getMatchingUsages](../android/media/AudioPlaybackCaptureConfiguration.md))`()` <br /> |
| [MediaProjection](../android/media/projection/MediaProjection.md) | [getMediaProjection](../android/media/AudioPlaybackCaptureConfiguration.md))`()` <br /> |

## Public methods

### getExcludeUids

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExcludeUids(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the UIDs passed to [Builder.excludeUid(int)](../android/media/AudioPlaybackCaptureConfiguration.Builder.md)). This value cannot be`null`. |

### getExcludeUsages

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExcludeUsages(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the usages passed to [Builder.excludeUsage(int)](../android/media/AudioPlaybackCaptureConfiguration.Builder.md)). Value is [android.media.AudioAttributes#USAGE_UNKNOWN](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_MEDIA](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_VOICE_COMMUNICATION](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_VOICE_COMMUNICATION_SIGNALLING](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ALARM](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_RINGTONE](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_REQUEST](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_INSTANT](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_DELAYED](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_EVENT](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ASSISTANCE_ACCESSIBILITY](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ASSISTANCE_NAVIGATION_GUIDANCE](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ASSISTANCE_SONIFICATION](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_GAME](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ASSISTANT](../android/media/AudioAttributes.md), android.media.AudioAttributes.USAGE_CALL_ASSISTANT, android.media.AudioAttributes.USAGE_EMERGENCY, android.media.AudioAttributes.USAGE_SAFETY, android.media.AudioAttributes.USAGE_VEHICLE_STATUS, android.media.AudioAttributes.USAGE_ANNOUNCEMENT, or android.media.AudioAttributes.USAGE_SPEAKER_CLEANUP This value cannot be`null`. |

### getMatchingUids

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatchingUids(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the UIDs passed to [Builder.addMatchingUid(int)](../android/media/AudioPlaybackCaptureConfiguration.Builder.md)). This value cannot be`null`. |

### getMatchingUsages

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatchingUsages(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the usages passed to [Builder.addMatchingUsage(int)](../android/media/AudioPlaybackCaptureConfiguration.Builder.md)). Value is [android.media.AudioAttributes#USAGE_UNKNOWN](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_MEDIA](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_VOICE_COMMUNICATION](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_VOICE_COMMUNICATION_SIGNALLING](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ALARM](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_RINGTONE](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_REQUEST](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_INSTANT](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_DELAYED](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_NOTIFICATION_EVENT](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ASSISTANCE_ACCESSIBILITY](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ASSISTANCE_NAVIGATION_GUIDANCE](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ASSISTANCE_SONIFICATION](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_GAME](../android/media/AudioAttributes.md), [android.media.AudioAttributes#USAGE_ASSISTANT](../android/media/AudioAttributes.md), android.media.AudioAttributes.USAGE_CALL_ASSISTANT, android.media.AudioAttributes.USAGE_EMERGENCY, android.media.AudioAttributes.USAGE_SAFETY, android.media.AudioAttributes.USAGE_VEHICLE_STATUS, android.media.AudioAttributes.USAGE_ANNOUNCEMENT, or android.media.AudioAttributes.USAGE_SPEAKER_CLEANUP This value cannot be`null`. |

### getMediaProjection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaProjection(): MediaProjection
```

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MediaProjection](../android/media/projection/MediaProjection.md) | the`MediaProjection`used to build this object. This value cannot be`null`. |

**See Also**

- [android.media.AudioPlaybackCaptureConfiguration.Builder#Builder(MediaProjection)](../android/media/AudioPlaybackCaptureConfiguration.Builder.md))
