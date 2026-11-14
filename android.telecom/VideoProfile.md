# VideoProfile

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VideoProfile

Kotlin| [Java](https://developer.android.com/reference/android/telecom/VideoProfile "View this page in Java") 

```
open class VideoProfile : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telecom.VideoProfile](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#) |

Represents attributes of video calls.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CameraCapabilities](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile.CameraCapabilities) Represents the camera capabilities important to a Video Telephony provider. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_DEFAULT](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_DEFAULT:kotlin.Int) Use default video quality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_HIGH:kotlin.Int) "High" video quality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_LOW](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_LOW:kotlin.Int) "Low" video quality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_MEDIUM](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_MEDIUM:kotlin.Int) "Medium" video quality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int) Used when answering or dialing a call to indicate that the call does not have a video component. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int) Video signal is bi-directional. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) Video is paused. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int) Video reception is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int) Video transmission is enabled. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VideoProfile](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#VideoProfile(kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an instance of the VideoProfile |
| [VideoProfile](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#VideoProfile(kotlin.Int,%20kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an instance of the VideoProfile |

| Public methods ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#describeContents())`()` Describe the kinds of special objects contained in this Parcelable's marshalled representation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQuality](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#getQuality())`()` The desired video quality for the call. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVideoState](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#getVideoState())`()` The video state of the call. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAudioOnly](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#isAudioOnly(kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state is audio only. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBidirectional](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#isBidirectional(kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state is bi-directional. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPaused](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#isPaused(kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state is paused. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReceptionEnabled](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#isReceptionEnabled(kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state has video reception enabled. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTransmissionEnabled](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#isTransmissionEnabled(kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state has video transmission enabled. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVideo](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#isVideo(kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether video transmission or reception is enabled for a video state. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#toString())`()` <br /> |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [videoStateToString](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#videoStateToString(kotlin.Int))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Generates a string representation of a video state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [VideoProfile](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#CREATOR:android.os.Parcelable.Creator) Responsible for creating VideoProfile objects from deserialized Parcels. |

## Constants

### QUALITY_DEFAULT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_DEFAULT: Int
```

Use default video quality. 

 Value: 4

### QUALITY_HIGH

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_HIGH: Int
```

"High" video quality. 

 Value: 1

### QUALITY_LOW

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_LOW: Int
```

"Low" video quality. 

 Value: 3

### QUALITY_MEDIUM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val QUALITY_MEDIUM: Int
```

"Medium" video quality. 

 Value: 2

### STATE_AUDIO_ONLY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_AUDIO_ONLY: Int
```

Used when answering or dialing a call to indicate that the call does not have a video component.

Should**not**be used in comparison checks to determine if a video state represents an audio-only call.

The following, for example, is not the correct way to check if a call is audio-only: 

```kotlin
<code>// This is the incorrect way to check for an audio-only call.
  if (videoState == VideoProfile.STATE_AUDIO_ONLY) {
       // Handle audio-only call.
  }
  </code>
```

Instead, use the [VideoProfile.isAudioOnly(int)](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#isAudioOnly(kotlin.Int))helper function to check if a video state represents an audio-only call: 

```kotlin
<code>// This is the correct way to check for an audio-only call.
  if (VideoProfile.isAudioOnly(videoState)) {
       // Handle audio-only call.
  }
  </code>
```  

 Value: 0

### STATE_BIDIRECTIONAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_BIDIRECTIONAL: Int
```

Video signal is bi-directional. 

 Value: 3

### STATE_PAUSED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_PAUSED: Int
```

Video is paused. 

 Value: 4

### STATE_RX_ENABLED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_RX_ENABLED: Int
```

Video reception is enabled. 

 Value: 2

### STATE_TX_ENABLED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_TX_ENABLED: Int
```

Video transmission is enabled. 

 Value: 1

## Public constructors

### VideoProfile

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VideoProfile(videoState: Int)
```

Creates an instance of the VideoProfile

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

### VideoProfile

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
VideoProfile(
    videoState: Int, 
    quality: Int)
```

Creates an instance of the VideoProfile

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video quality. Value is android.telecom.VideoProfile.QUALITY_UNKNOWN, [android.telecom.VideoProfile#QUALITY_HIGH](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_HIGH:kotlin.Int), [android.telecom.VideoProfile#QUALITY_MEDIUM](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_MEDIUM:kotlin.Int), [android.telecom.VideoProfile#QUALITY_LOW](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_LOW:kotlin.Int), or [android.telecom.VideoProfile#QUALITY_DEFAULT](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_DEFAULT:kotlin.Int) |

## Public methods

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable's marshalled representation.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshalled by the Parcelable. |

### getQuality

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getQuality(): Int
```

The desired video quality for the call. Valid values: [VideoProfile.QUALITY_HIGH](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_HIGH:kotlin.Int), [VideoProfile.QUALITY_MEDIUM](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_MEDIUM:kotlin.Int), [VideoProfile.QUALITY_LOW](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_LOW:kotlin.Int), [VideoProfile.QUALITY_DEFAULT](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_DEFAULT:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is android.telecom.VideoProfile.QUALITY_UNKNOWN, [android.telecom.VideoProfile#QUALITY_HIGH](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_HIGH:kotlin.Int), [android.telecom.VideoProfile#QUALITY_MEDIUM](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_MEDIUM:kotlin.Int), [android.telecom.VideoProfile#QUALITY_LOW](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_LOW:kotlin.Int), or [android.telecom.VideoProfile#QUALITY_DEFAULT](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#QUALITY_DEFAULT:kotlin.Int) |

### getVideoState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVideoState(): Int
```

The video state of the call. Valid values: [VideoProfile.STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [VideoProfile.STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), [VideoProfile.STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [VideoProfile.STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [VideoProfile.STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

### isAudioOnly

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isAudioOnly(videoState: Int): Boolean
```

Indicates whether the video state is audio only.

Note: Considers only whether either both the [STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int) or [STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int) bits are off, but not [STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `True`if the video state is audio only,`false`otherwise. |

### isBidirectional

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isBidirectional(videoState: Int): Boolean
```

Indicates whether the video state is bi-directional.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `True`if the video is bi-directional,`false`otherwise. |

### isPaused

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isPaused(videoState: Int): Boolean
```

Indicates whether the video state is paused.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `True`if the video is paused,`false`otherwise. |

### isReceptionEnabled

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isReceptionEnabled(videoState: Int): Boolean
```

Indicates whether the video state has video reception enabled.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `True`if video reception is enabled,`false`otherwise. |

### isTransmissionEnabled

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isTransmissionEnabled(videoState: Int): Boolean
```

Indicates whether the video state has video transmission enabled.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `True`if video transmission is enabled,`false`otherwise. |

### isVideo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isVideo(videoState: Int): Boolean
```

Indicates whether video transmission or reception is enabled for a video state.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `True`if video transmission or reception is enabled,`false`otherwise. |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### videoStateToString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun videoStateToString(videoState: Int): String!
```

Generates a string representation of a video state.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int), [android.telecom.VideoProfile#STATE_TX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_RX_ENABLED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int), and [android.telecom.VideoProfile#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_PAUSED:kotlin.Int) |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String representation of the video state. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<VideoProfile!>
```

Responsible for creating VideoProfile objects from deserialized Parcels.
