Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdBuffer

Kotlin | [Java](https://developer.android.com/reference/android/media/tv/AdBuffer "View this page in Java")

```
class AdBuffer : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.tv.AdBuffer](https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#) |

Buffer for advertisement data.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#AdBuffer(kotlin.Int,%20kotlin.String,%20android.os.SharedMemory,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20kotlin.Int)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, buffer: https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, presentationTimeUs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#getFlags()()` Gets the buffer flags for this ad buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#getId()()` Gets corresponding AD request ID. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#getLength()()` Gets the data length of this ad buffer. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#getMimeType()()` Gets the mime type of the data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#getOffset()()` Gets the offset into the shared memory to begin mapping. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#getPresentationTimeUs()()` Gets the presentation time. |
| [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#) | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#getSharedMemory()()` Gets the `https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#` which stores the data. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AdBuffer](https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#)!\> | `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### AdBuffer

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AdBuffer(
    id: Int, 
    mimeType: String, 
    buffer: SharedMemory, 
    offset: Int, 
    length: Int, 
    presentationTimeUs: Long, 
    flags: Int)
```

| Parameters ||
|---|---|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `buffer` | [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_SYNC_FRAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_KEY_FRAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_CODEC_CONFIG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_END_OF_STREAM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_PARTIAL_FRAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_DECODE_ONLY:kotlin.Int` |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getFlags

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFlags(): Int
```

Gets the buffer flags for this ad buffer.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The buffer flags for this ad buffer. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_SYNC_FRAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_KEY_FRAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_CODEC_CONFIG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_END_OF_STREAM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_PARTIAL_FRAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#BUFFER_FLAG_DECODE_ONLY:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodec.html#`

### getId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): Int
```

Gets corresponding AD request ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The ID of the ad request |

### getLength

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLength(): Int
```

Gets the data length of this ad buffer.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The data length of this ad buffer in bytes. |

### getMimeType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMimeType(): String
```

Gets the mime type of the data.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The mime type of the data. This value cannot be `null`. |

### getOffset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOffset(): Int
```

Gets the offset into the shared memory to begin mapping.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The offset of this ad buffer in the shared memory in bytes. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#map(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### getPresentationTimeUs

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPresentationTimeUs(): Long
```

Gets the presentation time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The presentation time in microseconds. |

### getSharedMemory

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSharedMemory(): SharedMemory
```

Gets the `https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#` which stores the data.

Information on how the data in this buffer is formatted can be found using `https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getMetadata()`

This data lives in a `https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#` instance because of the potentially large amount of data needed to store the ad. This optimizes the data communication between the ad data source and the service responsible for its display.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#` | The `https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#` that stores the data for this ad buffer. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#create(kotlin.String,%20kotlin.Int)`

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AdBuffer!>
```
