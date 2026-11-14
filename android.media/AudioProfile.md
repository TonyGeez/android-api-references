Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioProfile

```
open class AudioProfile : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioProfile](AudioProfile.md) |

An AudioProfile is specific to an audio format and lists supported sampling rates and channel masks for that format. An AudioDeviceInfo has a list of supported AudioProfiles. There can be multiple profiles whose encoding format is the same. This usually happens when an encoding format is only supported when it is encapsulated by some particular encapsulation types. If there are multiple encapsulation types that can carry this encoding format, they will be reported in different audio profiles. The application can choose any of the encapsulation types.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_IEC61937:kotlin.Int` Encapsulation format is defined in standard IEC 61937. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_NONE:kotlin.Int` No encapsulation type is specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_PCM:kotlin.Int` Encapsulation format is PCM, which can be used by other formats that can be wrapped in a PCM frame, such as DSD(Direct Stream Digital). |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | getChannelIndexMasks <br /> |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | getChannelMasks <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getEncapsulationType The encapsulation type indicates what encapsulation type is required when the framework is using this format when playing to a device exposing this audio profile. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getFormat <br /> |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | getSampleRates <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AudioProfile](AudioProfile.md)!\> | `https://developer.android.com/reference/kotlin/android/media/AudioProfile#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### AUDIO_ENCAPSULATION_TYPE_IEC61937

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_ENCAPSULATION_TYPE_IEC61937: Int
```

Encapsulation format is defined in standard IEC 61937.

 Value: 1

### AUDIO_ENCAPSULATION_TYPE_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_ENCAPSULATION_TYPE_NONE: Int
```

No encapsulation type is specified.

 Value: 0

### AUDIO_ENCAPSULATION_TYPE_PCM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUDIO_ENCAPSULATION_TYPE_PCM: Int
```

Encapsulation format is PCM, which can be used by other formats that can be wrapped in a PCM frame, such as DSD(Direct Stream Digital).

 Value: 2

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
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

### getChannelIndexMasks

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChannelIndexMasks(): IntArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | an array of channel index masks that are associated with the encoding format. This value cannot be `null`. |

### getChannelMasks

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChannelMasks(): IntArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | an array of channel position masks that are associated with the encoding format. This value cannot be `null`. |

### getEncapsulationType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEncapsulationType(): Int
```

The encapsulation type indicates what encapsulation type is required when the framework is using this format when playing to a device exposing this audio profile. When encapsulation is required, only playback with AudioTrack API is supported. But playback with MediaPlayer is not. When an encapsulation type is required, the AudioFormat encoding selected when creating the AudioTrack must match the encapsulation type, e.g AudioFormat.ENCODING_IEC61937 for AUDIO_ENCAPSULATION_TYPE_IEC61937.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an integer representing the encapsulation type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_IEC61937:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_PCM:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_IEC61937:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_PCM:kotlin.Int`

### getFormat

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFormat(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the encoding format for this AudioProfile. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DEFAULT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_16BIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_8BIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_FLOAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MP3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_LC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_HE_V1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_HE_V2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IEC61937:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_TRUEHD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_ELD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AAC_XHE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_AC4_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_E_AC3_JOC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DOLBY_MAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_OPUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_24BIT_PACKED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_PCM_32BIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_BL_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_MPEGH_LC_L4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DRA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_HD_MA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DTS_UHD_P2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_DSD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_AAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_FLAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_OPUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_ENHANCED_PROFILE_PCM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_AAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_FLAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_OPUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_BASE_PROFILE_PCM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_AAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_FLAC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_OPUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/AudioFormat#ENCODING_IAMF_SIMPLE_PROFILE_PCM:kotlin.Int` |

### getSampleRates

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSampleRates(): IntArray
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | an array of sample rates that are associated with the encoding format. This value cannot be `null`. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AudioProfile!>
```
