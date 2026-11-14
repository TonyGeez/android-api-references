# AdRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdRequest

Kotlin| [Java](../android/media/tv/AdRequest.md) 
| --- | --- |

```
class AdRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.AdRequest](../android/media/tv/AdRequest.md) |

An advertisement request which can be sent to TV input to request AD operations.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_START](../android/media/tv/AdRequest.md) Request to start an advertisement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_STOP](../android/media/tv/AdRequest.md) Request to stop an advertisement. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AdRequest](../android/media/tv/AdRequest.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `requestType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [Uri](../android/net/Uri.md)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `stopTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `echoInterval:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `metadata:` ` [Bundle](../android/os/Bundle.md)`)` <br /> |
| [AdRequest](../android/media/tv/AdRequest.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `requestType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fileDescriptor:` ` [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `stopTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `echoInterval:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mediaFileType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `metadata:` ` [Bundle](../android/os/Bundle.md)`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/tv/AdRequest.md))`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEchoIntervalMillis](../android/media/tv/AdRequest.md))`()` Gets the echo interval in milliseconds. |
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)? | [getFileDescriptor](../android/media/tv/AdRequest.md))`()` Gets the file descriptor of the AD media. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](../android/media/tv/AdRequest.md))`()` Gets the ID of AD request. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMediaFileType](../android/media/tv/AdRequest.md))`()` Gets the media file type such as mp4, mob, avi. |
| [Bundle](../android/os/Bundle.md) | [getMetadata](../android/media/tv/AdRequest.md))`()` Gets the metadata of the media file. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestType](../android/media/tv/AdRequest.md))`()` Gets the request type. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartTimeMillis](../android/media/tv/AdRequest.md))`()` Gets the start time of the AD media in milliseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStopTimeMillis](../android/media/tv/AdRequest.md))`()` Gets the stop time of the AD media in milliseconds. |
| --- | --- |
| [Uri](../android/net/Uri.md)? | [getUri](../android/media/tv/AdRequest.md))`()` Gets the URI of the AD media. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/tv/AdRequest.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AdRequest](../android/media/tv/AdRequest.md)!\> | [CREATOR](../android/media/tv/AdRequest.md) <br /> |

## Constants

### REQUEST_TYPE_START

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_TYPE_START: Int
```

Request to start an advertisement. 

 Value: 1

### REQUEST_TYPE_STOP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_TYPE_STOP: Int
```

Request to stop an advertisement. 

 Value: 2

## Public constructors

### AdRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AdRequest(
    id: Int, 
    requestType: Int, 
    uri: Uri?, 
    startTime: Long, 
    stopTime: Long, 
    echoInterval: Long, 
    metadata: Bundle)
```

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.AdRequest#REQUEST_TYPE_START](../android/media/tv/AdRequest.md), or [android.media.tv.AdRequest#REQUEST_TYPE_STOP](../android/media/tv/AdRequest.md) |
| `uri` | [Uri](../android/net/Uri.md)?:This value may be`null`. |
| `metadata` | [Bundle](../android/os/Bundle.md):This value cannot be`null`. |
| --- | --- |

### AdRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AdRequest(
    id: Int, 
    requestType: Int, 
    fileDescriptor: ParcelFileDescriptor?, 
    startTime: Long, 
    stopTime: Long, 
    echoInterval: Long, 
    mediaFileType: String?, 
    metadata: Bundle)
```

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.AdRequest#REQUEST_TYPE_START](../android/media/tv/AdRequest.md), or [android.media.tv.AdRequest#REQUEST_TYPE_STOP](../android/media/tv/AdRequest.md) |
| `fileDescriptor` | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)?:This value may be`null`. |
| `mediaFileType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| --- | --- |
| `metadata` | [Bundle](../android/os/Bundle.md):This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getEchoIntervalMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEchoIntervalMillis(): Long
```

Gets the echo interval in milliseconds.

The interval TV input needs to echo and inform TV interactive app service the video playback elapsed time. 
**See Also**

- [android.media.tv.AdResponse](../android/media/tv/AdResponse.md) 

### getFileDescriptor

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFileDescriptor(): ParcelFileDescriptor?
```

Gets the file descriptor of the AD media.

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)? | The file descriptor of the AD media. Can be`null`for [REQUEST_TYPE_STOP](../android/media/tv/AdRequest.md) or a URI is used. |

### getId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): Int
```

Gets the ID of AD request. 

### getMediaFileType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaFileType(): String?
```

Gets the media file type such as mp4, mob, avi.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The media file type. Can be`null`for [REQUEST_TYPE_STOP](../android/media/tv/AdRequest.md). |

### getMetadata

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetadata(): Bundle
```

Gets the metadata of the media file.

This includes additional information the TV input needs to play the AD media. This may include fields in [android.media.MediaFormat](../android/media/MediaFormat.md) like [android.media.MediaFormat#KEY_SAMPLE_RATE](../android/media/MediaFormat.md), or integrity information like SHA. What data is included depends on the format of the media file.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android/os/Bundle.md) | The metadata of the media file. Can be an empty bundle for [REQUEST_TYPE_STOP](../android/media/tv/AdRequest.md). This value cannot be`null`. |

### getRequestType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestType(): Int
```

Gets the request type.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.AdRequest#REQUEST_TYPE_START](../android/media/tv/AdRequest.md), or [android.media.tv.AdRequest#REQUEST_TYPE_STOP](../android/media/tv/AdRequest.md) |

### getStartTimeMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTimeMillis(): Long
```

Gets the start time of the AD media in milliseconds.

0 means start immediately 

### getStopTimeMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStopTimeMillis(): Long
```

Gets the stop time of the AD media in milliseconds.

-1 means until the end 

### getUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUri(): Uri?
```

Gets the URI of the AD media.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Uri](../android/net/Uri.md)? | The URI of the AD media. Can be`null`for [REQUEST_TYPE_STOP](../android/media/tv/AdRequest.md) or a file descriptor is used. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AdRequest!>
```
