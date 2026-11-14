# CamcorderProfile

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CamcorderProfile

Kotlin| [Java](https://developer.android.com/reference/android/media/CamcorderProfile "View this page in Java") 
| --- | --- |

```
open class CamcorderProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.CamcorderProfile](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#) |

Retrieves the predefined camcorder profile settings for camcorder applications. These settings are read-only.

The compressed output from a recording session with a given CamcorderProfile contains two tracks: one for audio and one for video.

Each profile specifies the following set of parameters:

- The file output format
- Video codec format
- Video bit rate in bits per second
- Video frame rate in frames per second
- Video frame width and height,
- Audio codec format
- Audio bit rate in bits per second,
- Audio sample rate
- Number of audio channels for recording.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_1080P:kotlin.Int) Quality level corresponding to the 1080p (1920 x 1080) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_2160P:kotlin.Int) Quality level corresponding to the 2160p (3840x2160) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_2K](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_2K:kotlin.Int) Quality level corresponding to 2K (2048 x 1080) resolution |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_480P:kotlin.Int) Quality level corresponding to the 480p (720 x 480) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_4KDCI](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_4KDCI:kotlin.Int) Quality level corresponding to 4k-DCI (4096 x 2160) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_720P:kotlin.Int) Quality level corresponding to the 720p (1280 x 720) resolution. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_8KUHD](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_8KUHD:kotlin.Int) Quality level corresponding to 8K UHD (7680 x 4320) resolution |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_CIF:kotlin.Int) Quality level corresponding to the cif (352 x 288) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH:kotlin.Int) Quality level corresponding to the highest available resolution. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH_SPEED_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_1080P:kotlin.Int) High speed ( \>= 100fps) quality level corresponding to the 1080p (1920 x 1080 or 1920x1088) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH_SPEED_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_2160P:kotlin.Int) High speed ( \>= 100fps) quality level corresponding to the 2160p (3840 x 2160) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH_SPEED_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_480P:kotlin.Int) High speed ( \>= 100fps) quality level corresponding to the 480p (720 x 480) resolution. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH_SPEED_4KDCI](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_4KDCI:kotlin.Int) High speed ( \>= 100fps) quality level corresponding to the 4K-DCI (4096 x 2160) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH_SPEED_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_720P:kotlin.Int) High speed ( \>= 100fps) quality level corresponding to the 720p (1280 x 720) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH_SPEED_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_CIF:kotlin.Int) High speed ( \>= 100fps) quality level corresponding to the CIF (352 x 288) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH_SPEED_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_HIGH:kotlin.Int) High speed ( \>= 100fps) quality level corresponding to the highest available resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH_SPEED_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_LOW:kotlin.Int) High speed ( \>= 100fps) quality level corresponding to the lowest available resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH_SPEED_VGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_VGA:kotlin.Int) High speed ( \>= 100fps) quality level corresponding to the VGA (640 x 480) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_LOW:kotlin.Int) Quality level corresponding to the lowest available resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_QCIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_QCIF:kotlin.Int) Quality level corresponding to the qcif (176 x 144) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_QHD](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_QHD:kotlin.Int) Quality level corresponding to QHD (2560 x 1440) resolution |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_QVGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_QVGA:kotlin.Int) Quality level corresponding to the QVGA (320x240) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_1080P:kotlin.Int) Time lapse quality level corresponding to the 1080p (1920 x 1088) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_2160P:kotlin.Int) Time lapse quality level corresponding to the 2160p (3840 x 2160) resolution. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_2K](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_2K:kotlin.Int) Time lapse quality level corresponding to the 2K (2048 x 1080) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_480P:kotlin.Int) Time lapse quality level corresponding to the 480p (720 x 480) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_4KDCI](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_4KDCI:kotlin.Int) Time lapse quality level corresponding to the 4k-DCI (4096 x 2160) resolution. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_720P:kotlin.Int) Time lapse quality level corresponding to the 720p (1280 x 720) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_8KUHD](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_8KUHD:kotlin.Int) Time lapse quality level corresponding to the 8K UHD (7680 x 4320) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_CIF:kotlin.Int) Time lapse quality level corresponding to the cif (352 x 288) resolution. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_HIGH:kotlin.Int) Time lapse quality level corresponding to the highest available resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_LOW:kotlin.Int) Time lapse quality level corresponding to the lowest available resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_QCIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_QCIF:kotlin.Int) Time lapse quality level corresponding to the qcif (176 x 144) resolution. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_QHD](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_QHD:kotlin.Int) Time lapse quality level corresponding to the QHD (2560 x 1440) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_QVGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_QVGA:kotlin.Int) Time lapse quality level corresponding to the QVGA (320 x 240) resolution. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_TIME_LAPSE_VGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_VGA:kotlin.Int) Time lapse quality level corresponding to the VGA (640 x 480) resolution. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_VGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_VGA:kotlin.Int) Quality level corresponding to the VGA (640 x 480) resolution. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CamcorderProfile](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#)! | [get](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#get(kotlin.Int))`(`quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the default camcorder profile at the given quality level for the first back-facing camera on the device. |
| openstatic [CamcorderProfile](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#)! | [get](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#get(kotlin.Int,%20kotlin.Int))`(`cameraId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the default camcorder profile for the given camera at the given quality level. |
| openstatic [EncoderProfiles](https://developer.android.com/reference/kotlin/android/media/EncoderProfiles)? | [getAll](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#getAll(kotlin.String,%20kotlin.Int))`(`cameraId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns all encoder profiles of a camcorder profile for the given camera at the given quality level. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasProfile](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#hasProfile(kotlin.Int))`(`quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if a camcorder profile exists for the first back-facing camera at the given quality level. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasProfile](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#hasProfile(kotlin.Int,%20kotlin.Int))`(`cameraId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if a camcorder profile exists for the given camera at the given quality level. |

| Properties ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [audioBitRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#audioBitRate:kotlin.Int) The target audio output bit rate in bits per second |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [audioChannels](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#audioChannels:kotlin.Int) The number of audio channels used for the audio track |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [audioCodec](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#audioCodec:kotlin.Int) The audio encoder being used for the audio track. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [audioSampleRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#audioSampleRate:kotlin.Int) The audio sampling rate used for the audio track |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [duration](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#duration:kotlin.Int) Default recording duration in seconds before the session is terminated. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [fileFormat](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#fileFormat:kotlin.Int) The file output format of the camcorder profile |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [quality](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#quality:kotlin.Int) The quality level of the camcorder profile |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [videoBitRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoBitRate:kotlin.Int) The target video output bit rate in bits per second |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [videoCodec](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoCodec:kotlin.Int) The video encoder being used for the video track |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [videoFrameHeight](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoFrameHeight:kotlin.Int) The target video frame height in pixels |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [videoFrameRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoFrameRate:kotlin.Int) The target video frame rate in frames per second. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [videoFrameWidth](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoFrameWidth:kotlin.Int) The target video frame width in pixels |
| --- | --- |

## Constants

### QUALITY_1080P

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_1080P: Int
```

Quality level corresponding to the 1080p (1920 x 1080) resolution. Note that the vertical resolution for 1080p can also be 1088, instead of 1080 (used by some vendors to avoid cropping during video playback). 

 Value: 6

### QUALITY_2160P

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_2160P: Int
```

Quality level corresponding to the 2160p (3840x2160) resolution. 

 Value: 8

### QUALITY_2K

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_2K: Int
```

Quality level corresponding to 2K (2048 x 1080) resolution 

 Value: 12

### QUALITY_480P

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_480P: Int
```

Quality level corresponding to the 480p (720 x 480) resolution. Note that the horizontal resolution for 480p can also be other values, such as 640 or 704, instead of 720. 

 Value: 4

### QUALITY_4KDCI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_4KDCI: Int
```

Quality level corresponding to 4k-DCI (4096 x 2160) resolution. 

 Value: 10

### QUALITY_720P

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_720P: Int
```

Quality level corresponding to the 720p (1280 x 720) resolution. 

 Value: 5

### QUALITY_8KUHD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_8KUHD: Int
```

Quality level corresponding to 8K UHD (7680 x 4320) resolution 

 Value: 13

### QUALITY_CIF

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_CIF: Int
```

Quality level corresponding to the cif (352 x 288) resolution. 

 Value: 3

### QUALITY_HIGH

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH: Int
```

Quality level corresponding to the highest available resolution. 

 Value: 1

### QUALITY_HIGH_SPEED_1080P

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH_SPEED_1080P: Int
```

High speed ( \>= 100fps) quality level corresponding to the 1080p (1920 x 1080 or 1920x1088) resolution. 

 Value: 2004

### QUALITY_HIGH_SPEED_2160P

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH_SPEED_2160P: Int
```

High speed ( \>= 100fps) quality level corresponding to the 2160p (3840 x 2160) resolution. 

 Value: 2005

### QUALITY_HIGH_SPEED_480P

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH_SPEED_480P: Int
```

High speed ( \>= 100fps) quality level corresponding to the 480p (720 x 480) resolution. Note that the horizontal resolution for 480p can also be other values, such as 640 or 704, instead of 720. 

 Value: 2002

### QUALITY_HIGH_SPEED_4KDCI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH_SPEED_4KDCI: Int
```

High speed ( \>= 100fps) quality level corresponding to the 4K-DCI (4096 x 2160) 

 Value: 2008

### QUALITY_HIGH_SPEED_720P

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH_SPEED_720P: Int
```

High speed ( \>= 100fps) quality level corresponding to the 720p (1280 x 720) resolution. 

 Value: 2003

### QUALITY_HIGH_SPEED_CIF

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH_SPEED_CIF: Int
```

High speed ( \>= 100fps) quality level corresponding to the CIF (352 x 288) 

 Value: 2006

### QUALITY_HIGH_SPEED_HIGH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH_SPEED_HIGH: Int
```

High speed ( \>= 100fps) quality level corresponding to the highest available resolution. 

 Value: 2001

### QUALITY_HIGH_SPEED_LOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH_SPEED_LOW: Int
```

High speed ( \>= 100fps) quality level corresponding to the lowest available resolution.

For all the high speed profiles defined below ((from [QUALITY_HIGH_SPEED_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_LOW:kotlin.Int) to [QUALITY_HIGH_SPEED_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_2160P:kotlin.Int)), they are similar as normal recording profiles, with just higher output frame rate and bit rate. Therefore, setting these profiles with [MediaRecorder.setProfile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setProfile(android.media.CamcorderProfile))without specifying any other encoding parameters will produce high speed videos rather than slow motion videos that have different capture and output (playback) frame rates. To record slow motion videos, the application must set video output (playback) frame rate and bit rate appropriately via [MediaRecorder.setVideoFrameRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoFrameRate(kotlin.Int))and [MediaRecorder.setVideoEncodingBitRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoEncodingBitRate(kotlin.Int))based on the slow motion factor. If the application intends to do the video recording with [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) encoder, it must set each individual field of [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) similarly according to this CamcorderProfile. 

 Value: 2000

**See Also**

- [#videoBitRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoBitRate:kotlin.Int)
- [#videoFrameRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoFrameRate:kotlin.Int)
- [android.media.MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder)
- [android.media.MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)
- [android.media.MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) 

### QUALITY_HIGH_SPEED_VGA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH_SPEED_VGA: Int
```

High speed ( \>= 100fps) quality level corresponding to the VGA (640 x 480) 

 Value: 2007

### QUALITY_LOW

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_LOW: Int
```

Quality level corresponding to the lowest available resolution. 

 Value: 0

### QUALITY_QCIF

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_QCIF: Int
```

Quality level corresponding to the qcif (176 x 144) resolution. 

 Value: 2

### QUALITY_QHD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_QHD: Int
```

Quality level corresponding to QHD (2560 x 1440) resolution 

 Value: 11

### QUALITY_QVGA

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_QVGA: Int
```

Quality level corresponding to the QVGA (320x240) resolution. 

 Value: 7

### QUALITY_TIME_LAPSE_1080P

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_1080P: Int
```

Time lapse quality level corresponding to the 1080p (1920 x 1088) resolution. 

 Value: 1006

### QUALITY_TIME_LAPSE_2160P

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_2160P: Int
```

Time lapse quality level corresponding to the 2160p (3840 x 2160) resolution. 

 Value: 1008

### QUALITY_TIME_LAPSE_2K

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_2K: Int
```

Time lapse quality level corresponding to the 2K (2048 x 1080) resolution. 

 Value: 1012

### QUALITY_TIME_LAPSE_480P

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_480P: Int
```

Time lapse quality level corresponding to the 480p (720 x 480) resolution. 

 Value: 1004

### QUALITY_TIME_LAPSE_4KDCI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_4KDCI: Int
```

Time lapse quality level corresponding to the 4k-DCI (4096 x 2160) resolution. 

 Value: 1010

### QUALITY_TIME_LAPSE_720P

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_720P: Int
```

Time lapse quality level corresponding to the 720p (1280 x 720) resolution. 

 Value: 1005

### QUALITY_TIME_LAPSE_8KUHD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_8KUHD: Int
```

Time lapse quality level corresponding to the 8K UHD (7680 x 4320) resolution. 

 Value: 1013

### QUALITY_TIME_LAPSE_CIF

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_CIF: Int
```

Time lapse quality level corresponding to the cif (352 x 288) resolution. 

 Value: 1003

### QUALITY_TIME_LAPSE_HIGH

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_HIGH: Int
```

Time lapse quality level corresponding to the highest available resolution. 

 Value: 1001

### QUALITY_TIME_LAPSE_LOW

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_LOW: Int
```

Time lapse quality level corresponding to the lowest available resolution. 

 Value: 1000

### QUALITY_TIME_LAPSE_QCIF

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_QCIF: Int
```

Time lapse quality level corresponding to the qcif (176 x 144) resolution. 

 Value: 1002

### QUALITY_TIME_LAPSE_QHD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_QHD: Int
```

Time lapse quality level corresponding to the QHD (2560 x 1440) resolution. 

 Value: 1011

### QUALITY_TIME_LAPSE_QVGA

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_QVGA: Int
```

Time lapse quality level corresponding to the QVGA (320 x 240) resolution. 

 Value: 1007

### QUALITY_TIME_LAPSE_VGA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_TIME_LAPSE_VGA: Int
```

Time lapse quality level corresponding to the VGA (640 x 480) resolution. 

 Value: 1009

### QUALITY_VGA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_VGA: Int
```

Quality level corresponding to the VGA (640 x 480) resolution. 

 Value: 9

## Public methods

### get

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun get(quality: Int): CamcorderProfile!
```

**Deprecated:** *Use [getAll](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#getAll(kotlin.String,%20kotlin.Int))instead*

Returns the default camcorder profile at the given quality level for the first back-facing camera on the device. If the device has no back-facing camera, this returns null.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------|
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the target quality level for the camcorder profile |

**See Also**

- [#get(int, int)](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#get(kotlin.Int,%20kotlin.Int)) 

### get

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun get(
    cameraId: Int, 
    quality: Int
): CamcorderProfile!
```

**Deprecated:** *Use [getAll](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#getAll(kotlin.String,%20kotlin.Int))instead*

Returns the default camcorder profile for the given camera at the given quality level. Quality levels QUALITY_LOW, QUALITY_HIGH are guaranteed to be supported, while other levels may or may not be supported. The supported levels can be checked using [hasProfile(int,int)](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#hasProfile(kotlin.Int,%20kotlin.Int)). QUALITY_LOW refers to the lowest quality available, while QUALITY_HIGH refers to the highest quality available. QUALITY_LOW/QUALITY_HIGH have to match one of qcif, cif, 480p, 720p, 1080p or 2160p. E.g. if the device supports 480p, 720p, 1080p and 2160p, then low is 480p and high is 2160p. The same is true for time lapse quality levels, i.e. QUALITY_TIME_LAPSE_LOW, QUALITY_TIME_LAPSE_HIGH are guaranteed to be supported and have to match one of qcif, cif, 480p, 720p, 1080p, or 2160p. For high speed quality levels, they may or may not be supported. If a subset of the levels are supported, QUALITY_HIGH_SPEED_LOW and QUALITY_HIGH_SPEED_HIGH are guaranteed to be supported and have to match one of 480p, 720p, or 1080p. A camcorder recording session with higher quality level usually has higher output bit rate, better video and/or audio recording quality, larger video frame resolution and higher audio sampling rate, etc, than those with lower quality level.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id for the camera. Integer camera ids parsed from the list received by invoking [CameraManager.getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#getCameraIdList())can be used as long as they are [CameraMetadata.REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int) and not [EXTERNAL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL:kotlin.Int). |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the target quality level for the camcorder profile. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if quality is not one of the defined QUALITY_ values. |

**See Also**

- [#QUALITY_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_LOW:kotlin.Int)
- [#QUALITY_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH:kotlin.Int)
- [#QUALITY_QCIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_QCIF:kotlin.Int)
- [#QUALITY_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_CIF:kotlin.Int)
- [#QUALITY_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_480P:kotlin.Int)
- [#QUALITY_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_720P:kotlin.Int)
- [#QUALITY_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_1080P:kotlin.Int)
- [#QUALITY_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_2160P:kotlin.Int)
- [#QUALITY_TIME_LAPSE_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_LOW:kotlin.Int)
- [#QUALITY_TIME_LAPSE_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_HIGH:kotlin.Int)
- [#QUALITY_TIME_LAPSE_QCIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_QCIF:kotlin.Int)
- [#QUALITY_TIME_LAPSE_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_CIF:kotlin.Int)
- [#QUALITY_TIME_LAPSE_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_480P:kotlin.Int)
- [#QUALITY_TIME_LAPSE_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_720P:kotlin.Int)
- [#QUALITY_TIME_LAPSE_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_1080P:kotlin.Int)
- [#QUALITY_TIME_LAPSE_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_2160P:kotlin.Int)
- [#QUALITY_HIGH_SPEED_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_LOW:kotlin.Int)
- [#QUALITY_HIGH_SPEED_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_HIGH:kotlin.Int)
- [#QUALITY_HIGH_SPEED_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_480P:kotlin.Int)
- [#QUALITY_HIGH_SPEED_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_720P:kotlin.Int)
- [#QUALITY_HIGH_SPEED_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_1080P:kotlin.Int)
- [#QUALITY_HIGH_SPEED_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_2160P:kotlin.Int) 

### getAll

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAll(
    cameraId: String, 
    quality: Int
): EncoderProfiles?
```

Returns all encoder profiles of a camcorder profile for the given camera at the given quality level.

Quality levels QUALITY_LOW, QUALITY_HIGH are guaranteed to be supported, while other levels may or may not be supported. The supported levels can be checked using [hasProfile(int,int)](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#hasProfile(kotlin.Int,%20kotlin.Int)). QUALITY_LOW refers to the lowest quality available, while QUALITY_HIGH refers to the highest quality available. QUALITY_LOW/QUALITY_HIGH have to match one of qcif, cif, 480p, 720p, 1080p or 2160p. E.g. if the device supports 480p, 720p, 1080p and 2160p, then low is 480p and high is 2160p.

The same is true for time lapse quality levels, i.e. QUALITY_TIME_LAPSE_LOW, QUALITY_TIME_LAPSE_HIGH are guaranteed to be supported and have to match one of qcif, cif, 480p, 720p, 1080p, or 2160p.

For high speed quality levels, they may or may not be supported. If a subset of the levels are supported, QUALITY_HIGH_SPEED_LOW and QUALITY_HIGH_SPEED_HIGH are guaranteed to be supported and have to match one of 480p, 720p, or 1080p.

A camcorder recording session with higher quality level usually has higher output bit rate, better video and/or audio recording quality, larger video frame resolution and higher audio sampling rate, etc, than those with lower quality level.

**Note:** as of [Android TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int), this method can return advanced encoder profiles.

Apps targeting [Build.VERSION_CODES.S_V2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S_V2:kotlin.Int) or before will only receive basic video encoder profiles that use output YUV 4:2:0 8-bit content. Apps targeting [Build.VERSION_CODES.TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int) or above will also receive advanced video encoder profiles that may output 10-bit, YUV 4:2:2/4:4:4 or HDR content.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the id for the camera. Numeric camera ids from the list received by invoking [CameraManager.getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#getCameraIdList())can be used as long as they are [CameraMetadata.REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int) and not [EXTERNAL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL:kotlin.Int). This value cannot be`null`. |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the target quality level for the camcorder profile. Value is [android.media.CamcorderProfile#QUALITY_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_LOW:kotlin.Int), [android.media.CamcorderProfile#QUALITY_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH:kotlin.Int), [android.media.CamcorderProfile#QUALITY_QCIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_QCIF:kotlin.Int), [android.media.CamcorderProfile#QUALITY_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_CIF:kotlin.Int), [android.media.CamcorderProfile#QUALITY_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_480P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_720P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_1080P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_QVGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_QVGA:kotlin.Int), [android.media.CamcorderProfile#QUALITY_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_2160P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_VGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_VGA:kotlin.Int), [android.media.CamcorderProfile#QUALITY_4KDCI](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_4KDCI:kotlin.Int), [android.media.CamcorderProfile#QUALITY_QHD](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_QHD:kotlin.Int), [android.media.CamcorderProfile#QUALITY_2K](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_2K:kotlin.Int), [android.media.CamcorderProfile#QUALITY_8KUHD](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_8KUHD:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_LOW:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_HIGH:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_QCIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_QCIF:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_CIF:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_480P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_720P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_1080P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_QVGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_QVGA:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_2160P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_VGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_VGA:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_4KDCI](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_4KDCI:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_QHD](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_QHD:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_2K](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_2K:kotlin.Int), [android.media.CamcorderProfile#QUALITY_TIME_LAPSE_8KUHD](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_8KUHD:kotlin.Int), [android.media.CamcorderProfile#QUALITY_HIGH_SPEED_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_LOW:kotlin.Int), [android.media.CamcorderProfile#QUALITY_HIGH_SPEED_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_HIGH:kotlin.Int), [android.media.CamcorderProfile#QUALITY_HIGH_SPEED_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_480P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_HIGH_SPEED_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_720P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_HIGH_SPEED_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_1080P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_HIGH_SPEED_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_2160P:kotlin.Int), [android.media.CamcorderProfile#QUALITY_HIGH_SPEED_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_CIF:kotlin.Int), [android.media.CamcorderProfile#QUALITY_HIGH_SPEED_VGA](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_VGA:kotlin.Int), or [android.media.CamcorderProfile#QUALITY_HIGH_SPEED_4KDCI](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_4KDCI:kotlin.Int) |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [EncoderProfiles](https://developer.android.com/reference/kotlin/android/media/EncoderProfiles)? | null if there are no encoder profiles defined for the quality level for the given camera. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if quality is not one of the defined QUALITY_ values. |

**See Also**

- [#QUALITY_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_LOW:kotlin.Int)
- [#QUALITY_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH:kotlin.Int)
- [#QUALITY_QCIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_QCIF:kotlin.Int)
- [#QUALITY_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_CIF:kotlin.Int)
- [#QUALITY_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_480P:kotlin.Int)
- [#QUALITY_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_720P:kotlin.Int)
- [#QUALITY_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_1080P:kotlin.Int)
- [#QUALITY_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_2160P:kotlin.Int)
- [#QUALITY_TIME_LAPSE_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_LOW:kotlin.Int)
- [#QUALITY_TIME_LAPSE_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_HIGH:kotlin.Int)
- [#QUALITY_TIME_LAPSE_QCIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_QCIF:kotlin.Int)
- [#QUALITY_TIME_LAPSE_CIF](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_CIF:kotlin.Int)
- [#QUALITY_TIME_LAPSE_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_480P:kotlin.Int)
- [#QUALITY_TIME_LAPSE_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_720P:kotlin.Int)
- [#QUALITY_TIME_LAPSE_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_1080P:kotlin.Int)
- [#QUALITY_TIME_LAPSE_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_TIME_LAPSE_2160P:kotlin.Int)
- [#QUALITY_HIGH_SPEED_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_LOW:kotlin.Int)
- [#QUALITY_HIGH_SPEED_HIGH](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_HIGH:kotlin.Int)
- [#QUALITY_HIGH_SPEED_480P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_480P:kotlin.Int)
- [#QUALITY_HIGH_SPEED_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_720P:kotlin.Int)
- [#QUALITY_HIGH_SPEED_1080P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_1080P:kotlin.Int)
- [#QUALITY_HIGH_SPEED_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_2160P:kotlin.Int) 

### hasProfile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun hasProfile(quality: Int): Boolean
```

Returns true if a camcorder profile exists for the first back-facing camera at the given quality level.

When using the Camera 2 API in`LEGACY`mode (i.e. when [android.hardware.camera2.CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key) is set to [android.hardware.camera2.CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int)), #hasProfile may return`true`for unsupported resolutions. To ensure a a given resolution is supported in LEGACY mode, the configuration given in [android.hardware.camera2.CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key) must contain the the resolution in the supported output sizes. The recommended way to check this is with [android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes(Class)](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap.html#getOutputSizes(java.lang.Class))with the class of the desired recording endpoint, and check that the desired resolution is contained in the list returned.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------|
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the target quality level for the camcorder profile |

**See Also**

- [android.hardware.camera2.CameraManager](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#)
- [android.hardware.camera2.CameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#) 

### hasProfile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun hasProfile(
    cameraId: Int, 
    quality: Int
): Boolean
```

Returns true if a camcorder profile exists for the given camera at the given quality level.

When using the Camera 2 API in LEGACY mode (i.e. when [android.hardware.camera2.CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#INFO_SUPPORTED_HARDWARE_LEVEL:android.hardware.camera2.CameraCharacteristics.Key) is set to [android.hardware.camera2.CameraCharacteristics#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#INFO_SUPPORTED_HARDWARE_LEVEL_LEGACY:kotlin.Int)), #hasProfile may return`true`for unsupported resolutions. To ensure a a given resolution is supported in LEGACY mode, the configuration given in [android.hardware.camera2.CameraCharacteristics#SCALER_STREAM_CONFIGURATION_MAP](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#SCALER_STREAM_CONFIGURATION_MAP:android.hardware.camera2.CameraCharacteristics.Key) must contain the the resolution in the supported output sizes. The recommended way to check this is with [android.hardware.camera2.params.StreamConfigurationMap#getOutputSizes(Class)](https://developer.android.com/reference/kotlin/android/hardware/camera2/params/StreamConfigurationMap.html#getOutputSizes(java.lang.Class))with the class of the desired recording endpoint, and check that the desired resolution is contained in the list returned.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cameraId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id for the camera. Integer camera ids parsed from the list received by invoking [CameraManager.getCameraIdList](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#getCameraIdList())can be used as long as they are [CameraMetadata.REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_BACKWARD_COMPATIBLE:kotlin.Int) and not [EXTERNAL](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraMetadata.html#INFO_SUPPORTED_HARDWARE_LEVEL_EXTERNAL:kotlin.Int). |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the target quality level for the camcorder profile |

**See Also**

- [android.hardware.camera2.CameraManager](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#)
- [android.hardware.camera2.CameraCharacteristics](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraCharacteristics.html#)

## Properties

### audioBitRate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var audioBitRate: Int
```

The target audio output bit rate in bits per second 

### audioChannels

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var audioChannels: Int
```

The number of audio channels used for the audio track 

### audioCodec

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var audioCodec: Int
```

The audio encoder being used for the audio track. 
**See Also**

- [android.media.MediaRecorder.AudioEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.AudioEncoder) 

### audioSampleRate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var audioSampleRate: Int
```

The audio sampling rate used for the audio track 

### duration

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var duration: Int
```

Default recording duration in seconds before the session is terminated. This is useful for applications like MMS has limited file size requirement. 

### fileFormat

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var fileFormat: Int
```

The file output format of the camcorder profile 
**See Also**

- [android.media.MediaRecorder.OutputFormat](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.OutputFormat) 

### quality

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var quality: Int
```

The quality level of the camcorder profile 

### videoBitRate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var videoBitRate: Int
```

The target video output bit rate in bits per second

This is the target recorded video output bit rate if the application configures the video recording via [MediaRecorder.setProfile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setProfile(android.media.CamcorderProfile))without specifying any other [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder) encoding parameters. For example, for high speed quality profiles (from [QUALITY_HIGH_SPEED_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_LOW:kotlin.Int) to [QUALITY_HIGH_SPEED_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_2160P:kotlin.Int)), this is the bit rate where the video is recorded with. If the application intends to record slow motion videos with the high speed quality profiles, it must set a different video bit rate that is corresponding to the desired recording output bit rate (i.e., the encoded video bit rate during normal playback) via [MediaRecorder.setVideoEncodingBitRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoEncodingBitRate(kotlin.Int)). For example, if [QUALITY_HIGH_SPEED_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_720P:kotlin.Int) advertises 240fps [videoFrameRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoFrameRate:kotlin.Int) and 64Mbps [videoBitRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoBitRate:kotlin.Int) in the high speed CamcorderProfile, and the application intends to record 1/8 factor slow motion recording videos, the application must set 30fps via [MediaRecorder.setVideoFrameRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoFrameRate(kotlin.Int))and 8Mbps ([videoBitRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoBitRate:kotlin.Int)\* slow motion factor) via [MediaRecorder.setVideoEncodingBitRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoEncodingBitRate(kotlin.Int)). Failing to do so will result in videos with unexpected frame rate and bit rate, or [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder) error if the output bit rate exceeds the encoder limit. If the application intends to do the video recording with [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) encoder, it must set each individual field of [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) similarly according to this CamcorderProfile. 
**See Also**

- [#videoFrameRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoFrameRate:kotlin.Int)
- [android.media.MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder)
- [android.media.MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)
- [android.media.MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) 

### videoCodec

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var videoCodec: Int
```

The video encoder being used for the video track 
**See Also**

- [android.media.MediaRecorder.VideoEncoder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.VideoEncoder) 

### videoFrameHeight

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var videoFrameHeight: Int
```

The target video frame height in pixels 

### videoFrameRate

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var videoFrameRate: Int
```

The target video frame rate in frames per second.

This is the target recorded video output frame rate per second if the application configures the video recording via [MediaRecorder.setProfile](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setProfile(android.media.CamcorderProfile))without specifying any other [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder) encoding parameters. For example, for high speed quality profiles (from [QUALITY_HIGH_SPEED_LOW](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_LOW:kotlin.Int) to [QUALITY_HIGH_SPEED_2160P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_2160P:kotlin.Int)), this is the frame rate where the video is recorded and played back with. If the application intends to create slow motion use case with the high speed quality profiles, it must set a different video frame rate that is corresponding to the desired output (playback) frame rate via [MediaRecorder.setVideoFrameRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoFrameRate(kotlin.Int)). For example, if [QUALITY_HIGH_SPEED_720P](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#QUALITY_HIGH_SPEED_720P:kotlin.Int) advertises 240fps [videoFrameRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoFrameRate:kotlin.Int) in the CamcorderProfile, and the application intends to create 1/8 factor slow motion recording videos, the application must set 30fps via [MediaRecorder.setVideoFrameRate](https://developer.android.com/reference/kotlin/android/media/MediaRecorder#setVideoFrameRate(kotlin.Int)). Failing to do so will result in high speed videos with normal speed playback frame rate (240fps for above example). If the application intends to do the video recording with [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec) encoder, it must set each individual field of [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) similarly according to this CamcorderProfile. 
**See Also**

- [#videoBitRate](https://developer.android.com/reference/kotlin/android/media/CamcorderProfile#videoBitRate:kotlin.Int)
- [android.media.MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder)
- [android.media.MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)
- [android.media.MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) 

### videoFrameWidth

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var videoFrameWidth: Int
```

The target video frame width in pixels
