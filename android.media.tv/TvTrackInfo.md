Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvTrackInfo

Kotlin | [Java](../android/media/tv/TvTrackInfo.md)
| --- | --- |

```
class TvTrackInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.TvTrackInfo](../android/media/tv/TvTrackInfo.md) |

Encapsulates the format of tracks played in `https://developer.android.com/reference/kotlin/android/media/tv/TvInputService`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo.Builder` A builder class for creating `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#` objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_AUDIO:kotlin.Int` The type value for audio tracks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_SUBTITLE:kotlin.Int` The type value for subtitle tracks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_VIDEO:kotlin.Int` The type value for video tracks. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getAudioChannelCount()()` Returns the audio channel count. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getAudioSampleRate()()` Returns the audio sample rate, in the unit of Hz. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getDescription()()` Returns a user readable description for the current track. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getEncoding()()` Returns the codec in the form of mime type. |
| --- | --- |
| [Bundle](../android/os/Bundle.md)! | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getExtra()()` Returns the extra information about the current track. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getId()()` Returns the ID of the track. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getLanguage()()` Returns the language information encoded by either ISO 639-1 or ISO 639-2/T. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getType()()` Returns the type of the track. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getVideoActiveFormatDescription()()` Returns the Active Format Description (AFD) code of the video. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getVideoFrameRate()()` Returns the frame rate of the video, in the unit of fps (frames per second). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getVideoHeight()()` Returns the height of the video, in the unit of pixels. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getVideoPixelAspectRatio()()` Returns the pixel aspect ratio (the ratio of a pixel's width to its height) of the video. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#getVideoWidth()()` Returns the width of the video, in the unit of pixels. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#isAudioDescription()()` Returns `true` if the track is an audio description intended for people with visual impairment, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#isEncrypted()()` Returns `true` if the track is encrypted, `false` otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#isHardOfHearing()()` Returns `true` if the track is intended for people with hearing impairment, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#isSpokenSubtitle()()` Returns `true` if the track is a spoken subtitle for people with visual impairment, `false` otherwise. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TvTrackInfo](../android/media/tv/TvTrackInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### TYPE_AUDIO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_AUDIO: Int
```

The type value for audio tracks.

 Value: 0

### TYPE_SUBTITLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SUBTITLE: Int
```

The type value for subtitle tracks.

 Value: 2

### TYPE_VIDEO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VIDEO: Int
```

The type value for video tracks.

 Value: 1

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAudioChannelCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAudioChannelCount(): Int
```

Returns the audio channel count. Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_AUDIO:kotlin.Int` tracks.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on an audio track |

### getAudioSampleRate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAudioSampleRate(): Int
```

Returns the audio sample rate, in the unit of Hz. Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_AUDIO:kotlin.Int` tracks.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on an audio track |

### getDescription

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDescription(): CharSequence!
```

Returns a user readable description for the current track.

### getEncoding

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEncoding(): String?
```

Returns the codec in the form of mime type. If the encoding is unknown or could not be determined, the corresponding value will be `null`.

For example of broadcast, codec information may be referred to broadcast standard (e.g. Component Descriptor of ETSI EN 300 468). In the case that track type is subtitle, mime type could be defined in broadcast standard (e.g. "text/dvb.subtitle" or "text/dvb.teletext" in ETSI TS 102 812 V1.3.1 section 7.6).

### getExtra

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtra(): Bundle!
```

Returns the extra information about the current track.

### getId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String!
```

Returns the ID of the track.

### getLanguage

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLanguage(): String!
```

Returns the language information encoded by either ISO 639-1 or ISO 639-2/T. If the language is unknown or could not be determined, the corresponding value will be `null`.

### getType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Returns the type of the track. The type should be one of the followings: `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_AUDIO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_VIDEO:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_SUBTITLE:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_AUDIO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_SUBTITLE:kotlin.Int` |

### getVideoActiveFormatDescription

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoActiveFormatDescription(): Byte
```

Returns the Active Format Description (AFD) code of the video. Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_VIDEO:kotlin.Int` tracks.

The complete list of values are defined in ETSI TS 101 154 V1.7.1 Annex B, ATSC A/53 Part 4 and SMPTE 2016-1-2007.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on a video track |

### getVideoFrameRate

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoFrameRate(): Float
```

Returns the frame rate of the video, in the unit of fps (frames per second). Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_VIDEO:kotlin.Int` tracks.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on a video track |

### getVideoHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoHeight(): Int
```

Returns the height of the video, in the unit of pixels. Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_VIDEO:kotlin.Int` tracks.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on a video track |

### getVideoPixelAspectRatio

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoPixelAspectRatio(): Float
```

Returns the pixel aspect ratio (the ratio of a pixel's width to its height) of the video. Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_VIDEO:kotlin.Int` tracks.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on a video track |

### getVideoWidth

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoWidth(): Int
```

Returns the width of the video, in the unit of pixels. Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_VIDEO:kotlin.Int` tracks.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on a video track |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isAudioDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAudioDescription(): Boolean
```

Returns `true` if the track is an audio description intended for people with visual impairment, `false` otherwise. Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_AUDIO:kotlin.Int` tracks.

For example of broadcast, audio description information may be referred to broadcast standard (e.g. ISO 639 Language Descriptor of ISO/IEC 13818-1, Supplementary Audio Language Descriptor, AC-3 Descriptor, Enhanced AC-3 Descriptor, AAC Descriptor of ETSI EN 300 468).

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on an audio track |

### isEncrypted

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEncrypted(): Boolean
```

Returns `true` if the track is encrypted, `false` otherwise. If the encryption status is unknown or could not be determined, the corresponding value will be `false`.

For example: ISO/IEC 13818-1 defines a CA descriptor that can be used to determine the encryption status of some broadcast streams.

### isHardOfHearing

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isHardOfHearing(): Boolean
```

Returns `true` if the track is intended for people with hearing impairment, `false` otherwise. Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_AUDIO:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_SUBTITLE:kotlin.Int` tracks.

For example of broadcast, hard of hearing information may be referred to broadcast standard (e.g. ISO 639 Language Descriptor of ISO/IEC 13818-1, Supplementary Audio Language Descriptor, AC-3 Descriptor, Enhanced AC-3 Descriptor, AAC Descriptor of ETSI EN 300 468).

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on an audio track or a subtitle track |

### isSpokenSubtitle

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSpokenSubtitle(): Boolean
```

Returns `true` if the track is a spoken subtitle for people with visual impairment, `false` otherwise. Valid only for `https://developer.android.com/reference/kotlin/android/media/tv/TvTrackInfo#TYPE_AUDIO:kotlin.Int` tracks.

For example of broadcast, spoken subtitle information may be referred to broadcast standard (e.g. Supplementary Audio Language Descriptor of ETSI EN 300 468).

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if not called on an audio track |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` to be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TvTrackInfo!>
```
