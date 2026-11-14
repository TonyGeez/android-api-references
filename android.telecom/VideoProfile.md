# VideoProfile

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VideoProfile

Kotlin| [Java](VideoProfile.md) 
| --- | --- |

```
open class VideoProfile : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.VideoProfile](VideoProfile.md) |

Represents attributes of video calls.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CameraCapabilities](../android/telecom/VideoProfile.CameraCapabilities.md) Represents the camera capabilities important to a Video Telephony provider. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_DEFAULT](VideoProfile.md) Use default video quality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_HIGH](VideoProfile.md) "High" video quality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_LOW](VideoProfile.md) "Low" video quality. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [QUALITY_MEDIUM](VideoProfile.md) "Medium" video quality. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_AUDIO_ONLY](VideoProfile.md) Used when answering or dialing a call to indicate that the call does not have a video component. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_BIDIRECTIONAL](VideoProfile.md) Video signal is bi-directional. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_PAUSED](VideoProfile.md) Video is paused. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_RX_ENABLED](VideoProfile.md) Video reception is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_TX_ENABLED](VideoProfile.md) Video transmission is enabled. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [VideoProfile](VideoProfile.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an instance of the VideoProfile |
| [VideoProfile](VideoProfile.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an instance of the VideoProfile |

| Public methods ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](VideoProfile.md))`()` Describe the kinds of special objects contained in this Parcelable's marshalled representation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQuality](VideoProfile.md))`()` The desired video quality for the call. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVideoState](VideoProfile.md))`()` The video state of the call. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAudioOnly](VideoProfile.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state is audio only. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBidirectional](VideoProfile.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state is bi-directional. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPaused](VideoProfile.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state is paused. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReceptionEnabled](VideoProfile.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state has video reception enabled. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTransmissionEnabled](VideoProfile.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the video state has video transmission enabled. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVideo](VideoProfile.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether video transmission or reception is enabled for a video state. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](VideoProfile.md))`()` <br /> |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [videoStateToString](VideoProfile.md))`(`videoState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Generates a string representation of a video state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](VideoProfile.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [VideoProfile](VideoProfile.md)!\> | [CREATOR](VideoProfile.md) Responsible for creating VideoProfile objects from deserialized Parcels. |

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

Instead, use the [VideoProfile.isAudioOnly(int)](VideoProfile.md))helper function to check if a video state represents an audio-only call: 

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
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |

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
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video quality. Value is android.telecom.VideoProfile.QUALITY_UNKNOWN, [android.telecom.VideoProfile#QUALITY_HIGH](VideoProfile.md), [android.telecom.VideoProfile#QUALITY_MEDIUM](VideoProfile.md), [android.telecom.VideoProfile#QUALITY_LOW](VideoProfile.md), or [android.telecom.VideoProfile#QUALITY_DEFAULT](VideoProfile.md) |

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

The desired video quality for the call. Valid values: [VideoProfile.QUALITY_HIGH](VideoProfile.md), [VideoProfile.QUALITY_MEDIUM](VideoProfile.md), [VideoProfile.QUALITY_LOW](VideoProfile.md), [VideoProfile.QUALITY_DEFAULT](VideoProfile.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is android.telecom.VideoProfile.QUALITY_UNKNOWN, [android.telecom.VideoProfile#QUALITY_HIGH](VideoProfile.md), [android.telecom.VideoProfile#QUALITY_MEDIUM](VideoProfile.md), [android.telecom.VideoProfile#QUALITY_LOW](VideoProfile.md), or [android.telecom.VideoProfile#QUALITY_DEFAULT](VideoProfile.md) |

### getVideoState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVideoState(): Int
```

The video state of the call. Valid values: [VideoProfile.STATE_AUDIO_ONLY](VideoProfile.md), [VideoProfile.STATE_BIDIRECTIONAL](VideoProfile.md), [VideoProfile.STATE_TX_ENABLED](VideoProfile.md), [VideoProfile.STATE_RX_ENABLED](VideoProfile.md), [VideoProfile.STATE_PAUSED](VideoProfile.md).

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |

### isAudioOnly

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isAudioOnly(videoState: Int): Boolean
```

Indicates whether the video state is audio only.

Note: Considers only whether either both the [STATE_RX_ENABLED](VideoProfile.md) or [STATE_TX_ENABLED](VideoProfile.md) bits are off, but not [STATE_PAUSED](VideoProfile.md).

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |

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
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |

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
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |

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
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |

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
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |

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
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |

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
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The video state. Value is either`0`or a combination of [android.telecom.VideoProfile#STATE_AUDIO_ONLY](VideoProfile.md), [android.telecom.VideoProfile#STATE_TX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_RX_ENABLED](VideoProfile.md), [android.telecom.VideoProfile#STATE_BIDIRECTIONAL](VideoProfile.md), and [android.telecom.VideoProfile#STATE_PAUSED](VideoProfile.md) |

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
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<VideoProfile!>
```

Responsible for creating VideoProfile objects from deserialized Parcels.
