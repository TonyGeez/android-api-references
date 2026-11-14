# AudioDescriptor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioDescriptor

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioDescriptor "View this page in Java") 
| --- | --- |

```
open class AudioDescriptor : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioDescriptor](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#) |

The AudioDescriptor contains the information to describe the audio playback/capture capabilities. The capabilities are described by a byte array, which is defined by a particular standard. This is used when the format is unrecognized to the platform.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDARD_EDID](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#STANDARD_EDID:kotlin.Int) The Extended Display Identification Data (EDID) standard for a short audio descriptor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDARD_NONE](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#STANDARD_NONE:kotlin.Int) The audio standard is not specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDARD_SADB](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#STANDARD_SADB:kotlin.Int) The standard for a Speaker Allocation Data Block (SADB). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDARD_VSADB](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#STANDARD_VSADB:kotlin.Int) The standard for a Vendor-Specific Audio Data Block (VSADB). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#describeContents())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getDescriptor](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#getDescriptor())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEncapsulationType](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#getEncapsulationType())`()` The encapsulation type indicates what encapsulation type is required when the framework is using this extra audio descriptor for playing to a device exposing this audio profile. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStandard](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#getStandard())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#hashCode())`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AudioDescriptor](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### STANDARD_EDID

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDARD_EDID: Int
```

The Extended Display Identification Data (EDID) standard for a short audio descriptor. 

 Value: 1

### STANDARD_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDARD_NONE: Int
```

The audio standard is not specified. 

 Value: 0

### STANDARD_SADB

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDARD_SADB: Int
```

The standard for a Speaker Allocation Data Block (SADB). 

 Value: 2

### STANDARD_VSADB

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDARD_VSADB: Int
```

The standard for a Vendor-Specific Audio Data Block (VSADB). 

 Value: 3

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDescriptor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDescriptor(): ByteArray
```

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | a byte array that describes audio playback/capture capabilities as encoded by the standard for this AudioDescriptor. This value cannot be`null`. |

### getEncapsulationType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncapsulationType(): Int
```

The encapsulation type indicates what encapsulation type is required when the framework is using this extra audio descriptor for playing to a device exposing this audio profile. When encapsulation is required, only playback with [android.media.AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack) API is supported. But playback with [android.media.MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer) is not. When an encapsulation type is required, the [AudioFormat](https://developer.android.com/reference/kotlin/android/media/AudioFormat) encoding selected when creating the [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack) must match the encapsulation type, e.g. AudioFormat#ENCODING_IEC61937 for AudioProfile.AUDIO_ENCAPSULATION_TYPE_IEC61937.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an integer representing the encapsulation type Value is [android.media.AudioProfile#AUDIO_ENCAPSULATION_TYPE_NONE](https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_NONE:kotlin.Int), [android.media.AudioProfile#AUDIO_ENCAPSULATION_TYPE_IEC61937](https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_IEC61937:kotlin.Int), or [android.media.AudioProfile#AUDIO_ENCAPSULATION_TYPE_PCM](https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_PCM:kotlin.Int) |

**See Also**

- [android.media.AudioProfile#AUDIO_ENCAPSULATION_TYPE_NONE](https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_NONE:kotlin.Int)
- [android.media.AudioProfile#AUDIO_ENCAPSULATION_TYPE_IEC61937](https://developer.android.com/reference/kotlin/android/media/AudioProfile#AUDIO_ENCAPSULATION_TYPE_IEC61937:kotlin.Int) 

### getStandard

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStandard(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the standard that defines audio playback/capture capabilities. Value is [android.media.AudioDescriptor#STANDARD_NONE](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#STANDARD_NONE:kotlin.Int), [android.media.AudioDescriptor#STANDARD_EDID](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#STANDARD_EDID:kotlin.Int), [android.media.AudioDescriptor#STANDARD_SADB](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#STANDARD_SADB:kotlin.Int), or [android.media.AudioDescriptor#STANDARD_VSADB](https://developer.android.com/reference/kotlin/android/media/AudioDescriptor#STANDARD_VSADB:kotlin.Int) |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AudioDescriptor!>
```
