# AdRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdRequest

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/AdRequest "View this page in Java") 

```
class AdRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.tv.AdRequest](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#) |

An advertisement request which can be sent to TV input to request AD operations.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_START](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_START:kotlin.Int) Request to start an advertisement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_STOP](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_STOP:kotlin.Int) Request to stop an advertisement. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AdRequest](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#AdRequest(kotlin.Int,%20kotlin.Int,%20android.net.Uri,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20android.os.Bundle))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `requestType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `stopTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `echoInterval:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `metadata:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` <br /> |
| [AdRequest](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#AdRequest(kotlin.Int,%20kotlin.Int,%20android.os.ParcelFileDescriptor,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.String,%20android.os.Bundle))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `requestType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fileDescriptor:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)?`, `startTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `stopTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `echoInterval:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mediaFileType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `metadata:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#describeContents())`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEchoIntervalMillis](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getEchoIntervalMillis())`()` Gets the echo interval in milliseconds. |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | [getFileDescriptor](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getFileDescriptor())`()` Gets the file descriptor of the AD media. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getId())`()` Gets the ID of AD request. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMediaFileType](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getMediaFileType())`()` Gets the media file type such as mp4, mob, avi. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getMetadata](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getMetadata())`()` Gets the metadata of the media file. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestType](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getRequestType())`()` Gets the request type. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartTimeMillis](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getStartTimeMillis())`()` Gets the start time of the AD media in milliseconds. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStopTimeMillis](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getStopTimeMillis())`()` Gets the stop time of the AD media in milliseconds. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getUri](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#getUri())`()` Gets the URI of the AD media. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AdRequest](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| `requestType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.AdRequest#REQUEST_TYPE_START](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_START:kotlin.Int), or [android.media.tv.AdRequest#REQUEST_TYPE_STOP](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_STOP:kotlin.Int) |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?:This value may be`null`. |
| `metadata` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):This value cannot be`null`. |

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
| `requestType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.AdRequest#REQUEST_TYPE_START](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_START:kotlin.Int), or [android.media.tv.AdRequest#REQUEST_TYPE_STOP](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_STOP:kotlin.Int) |
| `fileDescriptor` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)?:This value may be`null`. |
| `mediaFileType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `metadata` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getEchoIntervalMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEchoIntervalMillis(): Long
```

Gets the echo interval in milliseconds.

The interval TV input needs to echo and inform TV interactive app service the video playback elapsed time. 
**See Also**

- [android.media.tv.AdResponse](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse) 

### getFileDescriptor

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFileDescriptor(): ParcelFileDescriptor?
```

Gets the file descriptor of the AD media.

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)? | The file descriptor of the AD media. Can be`null`for [REQUEST_TYPE_STOP](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_STOP:kotlin.Int) or a URI is used. |

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
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The media file type. Can be`null`for [REQUEST_TYPE_STOP](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_STOP:kotlin.Int). |

### getMetadata

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetadata(): Bundle
```

Gets the metadata of the media file.

This includes additional information the TV input needs to play the AD media. This may include fields in [android.media.MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat.html#) like [android.media.MediaFormat#KEY_SAMPLE_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat.html#KEY_SAMPLE_RATE:kotlin.String), or integrity information like SHA. What data is included depends on the format of the media file.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | The metadata of the media file. Can be an empty bundle for [REQUEST_TYPE_STOP](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_STOP:kotlin.Int). This value cannot be`null`. |

### getRequestType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestType(): Int
```

Gets the request type.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.AdRequest#REQUEST_TYPE_START](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_START:kotlin.Int), or [android.media.tv.AdRequest#REQUEST_TYPE_STOP](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_STOP:kotlin.Int) |

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
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | The URI of the AD media. Can be`null`for [REQUEST_TYPE_STOP](https://developer.android.com/reference/kotlin/android/media/tv/AdRequest#REQUEST_TYPE_STOP:kotlin.Int) or a file descriptor is used. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AdRequest!>
```
