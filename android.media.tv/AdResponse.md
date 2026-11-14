# AdResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdResponse

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/AdResponse "View this page in Java") 

```
class AdResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.tv.AdResponse](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#) |

An advertisement response which can be sent to TV interactive App service to inform AD status.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_TYPE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_BUFFERING:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_TYPE_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_ERROR:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_TYPE_FINISHED](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_FINISHED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_TYPE_PLAYING](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_PLAYING:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_TYPE_STOPPED](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_STOPPED:kotlin.Int) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AdResponse](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#AdResponse(kotlin.Int,%20kotlin.Int,%20kotlin.Long))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `responseType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `elapsedTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#describeContents())`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getElapsedTimeMillis](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#getElapsedTimeMillis())`()` Gets the playback elapsed time in milliseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#getId())`()` Gets the ID of AD response. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResponseType](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#getResponseType())`()` Gets the response type. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AdResponse](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### RESPONSE_TYPE_BUFFERING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_TYPE_BUFFERING: Int
```  

 Value: 5

### RESPONSE_TYPE_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_TYPE_ERROR: Int
```  

 Value: 4

### RESPONSE_TYPE_FINISHED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_TYPE_FINISHED: Int
```  

 Value: 2

### RESPONSE_TYPE_PLAYING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_TYPE_PLAYING: Int
```  

 Value: 1

### RESPONSE_TYPE_STOPPED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_TYPE_STOPPED: Int
```  

 Value: 3

## Public constructors

### AdResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AdResponse(
    id: Int, 
    responseType: Int, 
    elapsedTime: Long)
```

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `responseType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.AdResponse#RESPONSE_TYPE_PLAYING](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_PLAYING:kotlin.Int), [android.media.tv.AdResponse#RESPONSE_TYPE_FINISHED](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_FINISHED:kotlin.Int), [android.media.tv.AdResponse#RESPONSE_TYPE_STOPPED](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_STOPPED:kotlin.Int), [android.media.tv.AdResponse#RESPONSE_TYPE_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_ERROR:kotlin.Int), or [android.media.tv.AdResponse#RESPONSE_TYPE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_BUFFERING:kotlin.Int) |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getElapsedTimeMillis

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getElapsedTimeMillis(): Long
```

Gets the playback elapsed time in milliseconds.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The playback elapsed time. -1 if no valid elapsed time. |

### getId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): Int
```

Gets the ID of AD response. 

### getResponseType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResponseType(): Int
```

Gets the response type.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.AdResponse#RESPONSE_TYPE_PLAYING](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_PLAYING:kotlin.Int), [android.media.tv.AdResponse#RESPONSE_TYPE_FINISHED](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_FINISHED:kotlin.Int), [android.media.tv.AdResponse#RESPONSE_TYPE_STOPPED](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_STOPPED:kotlin.Int), [android.media.tv.AdResponse#RESPONSE_TYPE_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_ERROR:kotlin.Int), or [android.media.tv.AdResponse#RESPONSE_TYPE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/tv/AdResponse#RESPONSE_TYPE_BUFFERING:kotlin.Int) |

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
static val CREATOR: Parcelable.Creator<AdResponse!>
```
