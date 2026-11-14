# AudioPlaybackCaptureConfiguration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioPlaybackCaptureConfiguration

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioPlaybackCaptureConfiguration "View this page in Java") 
| --- | --- |

```
class AudioPlaybackCaptureConfiguration
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioPlaybackCaptureConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration#) |

Configuration for capturing audio played by other apps. When capturing audio signals played by other apps (and yours), you will only capture a mix of the audio signals played by players (such as AudioTrack or MediaPlayer) which present the following characteristics:

- the usage value MUST be [AudioAttributes.USAGE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_UNKNOWN:kotlin.Int) or [AudioAttributes.USAGE_GAME](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_GAME:kotlin.Int) or [AudioAttributes.USAGE_MEDIA](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_MEDIA:kotlin.Int). All other usages CAN NOT be captured.
- AND the capture policy set by their app (with [AudioManager.setAllowedCapturePolicy](https://developer.android.com/reference/kotlin/android/media/AudioManager#setAllowedCapturePolicy(kotlin.Int))) or on each player (with [AudioAttributes.Builder.setAllowedCapturePolicy](https://developer.android.com/reference/kotlin/android/media/AudioAttributes.Builder#setAllowedCapturePolicy(kotlin.Int))) is [AudioAttributes.ALLOW_CAPTURE_BY_ALL](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#ALLOW_CAPTURE_BY_ALL:kotlin.Int), whichever is the most strict.
- AND their app attribute allowAudioPlaybackCapture in their manifest MUST either be:
 - set to "true"
 - not set, and their`targetSdkVersion`MUST be equal to or greater than [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). Ie. Apps that do not target at least Android Q must explicitly opt-in to be captured by a MediaProjection.
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
| | [Builder](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration.Builder) Builder for creating [AudioPlaybackCaptureConfiguration](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration#) instances. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getExcludeUids](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration#getExcludeUids())`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getExcludeUsages](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration#getExcludeUsages())`()` <br /> |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getMatchingUids](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration#getMatchingUids())`()` <br /> |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getMatchingUsages](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration#getMatchingUsages())`()` <br /> |
| [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) | [getMediaProjection](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration#getMediaProjection())`()` <br /> |

## Public methods

### getExcludeUids

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExcludeUids(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the UIDs passed to [Builder.excludeUid(int)](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration.Builder#excludeUid(kotlin.Int)). This value cannot be`null`. |

### getExcludeUsages

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExcludeUsages(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the usages passed to [Builder.excludeUsage(int)](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration.Builder#excludeUsage(kotlin.Int)). Value is [android.media.AudioAttributes#USAGE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_UNKNOWN:kotlin.Int), [android.media.AudioAttributes#USAGE_MEDIA](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_MEDIA:kotlin.Int), [android.media.AudioAttributes#USAGE_VOICE_COMMUNICATION](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_VOICE_COMMUNICATION:kotlin.Int), [android.media.AudioAttributes#USAGE_VOICE_COMMUNICATION_SIGNALLING](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_VOICE_COMMUNICATION_SIGNALLING:kotlin.Int), [android.media.AudioAttributes#USAGE_ALARM](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ALARM:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_RINGTONE](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_RINGTONE:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_REQUEST](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_REQUEST:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_INSTANT](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_INSTANT:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_DELAYED](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_DELAYED:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_EVENT](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_EVENT:kotlin.Int), [android.media.AudioAttributes#USAGE_ASSISTANCE_ACCESSIBILITY](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ASSISTANCE_ACCESSIBILITY:kotlin.Int), [android.media.AudioAttributes#USAGE_ASSISTANCE_NAVIGATION_GUIDANCE](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ASSISTANCE_NAVIGATION_GUIDANCE:kotlin.Int), [android.media.AudioAttributes#USAGE_ASSISTANCE_SONIFICATION](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ASSISTANCE_SONIFICATION:kotlin.Int), [android.media.AudioAttributes#USAGE_GAME](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_GAME:kotlin.Int), [android.media.AudioAttributes#USAGE_ASSISTANT](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ASSISTANT:kotlin.Int), android.media.AudioAttributes.USAGE_CALL_ASSISTANT, android.media.AudioAttributes.USAGE_EMERGENCY, android.media.AudioAttributes.USAGE_SAFETY, android.media.AudioAttributes.USAGE_VEHICLE_STATUS, android.media.AudioAttributes.USAGE_ANNOUNCEMENT, or android.media.AudioAttributes.USAGE_SPEAKER_CLEANUP This value cannot be`null`. |

### getMatchingUids

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatchingUids(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the UIDs passed to [Builder.addMatchingUid(int)](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration.Builder#addMatchingUid(kotlin.Int)). This value cannot be`null`. |

### getMatchingUsages

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatchingUsages(): IntArray
```

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the usages passed to [Builder.addMatchingUsage(int)](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration.Builder#addMatchingUsage(kotlin.Int)). Value is [android.media.AudioAttributes#USAGE_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_UNKNOWN:kotlin.Int), [android.media.AudioAttributes#USAGE_MEDIA](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_MEDIA:kotlin.Int), [android.media.AudioAttributes#USAGE_VOICE_COMMUNICATION](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_VOICE_COMMUNICATION:kotlin.Int), [android.media.AudioAttributes#USAGE_VOICE_COMMUNICATION_SIGNALLING](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_VOICE_COMMUNICATION_SIGNALLING:kotlin.Int), [android.media.AudioAttributes#USAGE_ALARM](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ALARM:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_RINGTONE](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_RINGTONE:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_REQUEST](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_REQUEST:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_INSTANT](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_INSTANT:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_DELAYED](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_COMMUNICATION_DELAYED:kotlin.Int), [android.media.AudioAttributes#USAGE_NOTIFICATION_EVENT](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_NOTIFICATION_EVENT:kotlin.Int), [android.media.AudioAttributes#USAGE_ASSISTANCE_ACCESSIBILITY](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ASSISTANCE_ACCESSIBILITY:kotlin.Int), [android.media.AudioAttributes#USAGE_ASSISTANCE_NAVIGATION_GUIDANCE](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ASSISTANCE_NAVIGATION_GUIDANCE:kotlin.Int), [android.media.AudioAttributes#USAGE_ASSISTANCE_SONIFICATION](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ASSISTANCE_SONIFICATION:kotlin.Int), [android.media.AudioAttributes#USAGE_GAME](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_GAME:kotlin.Int), [android.media.AudioAttributes#USAGE_ASSISTANT](https://developer.android.com/reference/kotlin/android/media/AudioAttributes#USAGE_ASSISTANT:kotlin.Int), android.media.AudioAttributes.USAGE_CALL_ASSISTANT, android.media.AudioAttributes.USAGE_EMERGENCY, android.media.AudioAttributes.USAGE_SAFETY, android.media.AudioAttributes.USAGE_VEHICLE_STATUS, android.media.AudioAttributes.USAGE_ANNOUNCEMENT, or android.media.AudioAttributes.USAGE_SPEAKER_CLEANUP This value cannot be`null`. |

### getMediaProjection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaProjection(): MediaProjection
```

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) | the`MediaProjection`used to build this object. This value cannot be`null`. |

**See Also**

- [android.media.AudioPlaybackCaptureConfiguration.Builder#Builder(MediaProjection)](https://developer.android.com/reference/kotlin/android/media/AudioPlaybackCaptureConfiguration.Builder#Builder(android.media.projection.MediaProjection))
