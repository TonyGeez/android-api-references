Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EncoderProfiles

Kotlin | [Java](../android/media/EncoderProfiles.md)
| --- | --- |

```
class EncoderProfiles
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.EncoderProfiles](../android/media/EncoderProfiles.md) |

Describes a set of encoding profiles for a given media (audio and/or video) profile. These settings are read-only.

Currently, this is used to describe camera recording profile with more detail than `https://developer.android.com/reference/kotlin/android/media/CamcorderProfile`, by providing encoding parameters for more than just the default audio and/or video codec.

The compressed output from a camera recording session contains two tracks: one for audio and one for video.

In the future audio-only recording profiles may be defined.

Each media profile specifies a set of audio and a set of video specific settings.

- The file output format
- Default file duration Video-specific settings are:

- Video codec format
- Video bit rate in bits per second
- Video frame rate in frames per second
- Video frame width and height,
- Video encoder profile. Audio-specific settings are:

- Audio codec format
- Audio bit rate in bits per second,
- Audio sample rate
- Number of audio channels for recording.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/EncoderProfiles.AudioProfile` Configuration for an audio encoder. |
| | `https://developer.android.com/reference/kotlin/android/media/EncoderProfiles.VideoProfile` Configuration for a video encoder. |

| Public methods ||
|---|---|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EncoderProfiles.AudioProfile](../android/media/EncoderProfiles.AudioProfile.md)!\> | `https://developer.android.com/reference/kotlin/android/media/EncoderProfiles#getAudioProfiles()()` Returns the defined audio encoder profiles. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/EncoderProfiles#getDefaultDurationSeconds()()` Default recording duration in seconds before the session is terminated. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/EncoderProfiles#getRecommendedFileFormat()()` Recommended output file format |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EncoderProfiles.VideoProfile](../android/media/EncoderProfiles.VideoProfile.md)!\> | `https://developer.android.com/reference/kotlin/android/media/EncoderProfiles#getVideoProfiles()()` Returns the defined video encoder profiles. |

## Public methods

### getAudioProfiles

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAudioProfiles(): MutableList<EncoderProfiles.AudioProfile!>
```

Returns the defined audio encoder profiles.

The list may be empty. This means there are no audio encoder profiles defined. Otherwise, the first profile is the default audio profile.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/EncoderProfiles.AudioProfile!>` | This value cannot be `null`. |

### getDefaultDurationSeconds

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDefaultDurationSeconds(): Int
```

Default recording duration in seconds before the session is terminated. This is useful for applications like MMS that have a limited file size requirement. This could be 0 if there is no default recording duration.

### getRecommendedFileFormat

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRecommendedFileFormat(): Int
```

Recommended output file format

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#THREE_GPP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#MPEG_4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#AMR_NB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#AMR_WB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#AAC_ADTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#MPEG_2_TS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#WEBM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat#OGG:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat`

### getVideoProfiles

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoProfiles(): MutableList<EncoderProfiles.VideoProfile!>
```

Returns the defined video encoder profiles.

The list may be empty. This means there are no video encoder profiles defined. Otherwise, the first profile is the default video profile.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/EncoderProfiles.VideoProfile!>` | This value cannot be `null`. |
