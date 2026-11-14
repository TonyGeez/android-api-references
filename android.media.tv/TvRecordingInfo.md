# TvRecordingInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvRecordingInfo

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/TvRecordingInfo "View this page in Java") 

```
class TvRecordingInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.tv.TvRecordingInfo](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#) |

This class is used to describe the meta information for a TV recording. It can be retrieved by the [android.media.tv.interactive.TvInteractiveAppService](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppService) by using getTvRecordingInfo or getTvRecordingInfoList. It can then be updated to the TV app using setTvRecordingInfo.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRIDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#FRIDAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MONDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#MONDAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_ALL](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#RECORDING_ALL:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_IN_PROGRESS](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#RECORDING_IN_PROGRESS:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RECORDING_SCHEDULED](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#RECORDING_SCHEDULED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SATURDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#SATURDAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUNDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#SUNDAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THURSDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#THURSDAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TUESDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#TUESDAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEDNESDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#WEDNESDAY:kotlin.Int) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TvRecordingInfo](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#TvRecordingInfo(kotlin.String,%20kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.String,%20kotlin.String,%20kotlin.Long,%20kotlin.Long,%20android.net.Uri,%20android.net.Uri,%20kotlin.collections.MutableList,%20android.net.Uri,%20kotlin.Long,%20kotlin.Long))`(`recordingId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `startPadding:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `endPadding:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `repeatDays:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `scheduledStartTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `scheduledDuration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `channelUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `programUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`, `contentRatings:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating)!>`, `recordingUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`, `recordingStartTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `recordingDuration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#describeContents())`()` <br /> |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getChannelUri](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getChannelUri())`()` Returns the uri of the broadcast channel where the recording will take place. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating)!\> | [getContentRatings](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getContentRatings())`()` Returns a list of content ratings for the program(s) in this recording. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDescription](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getDescription())`()` Returns the description of the scheduled recording. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEndPaddingMillis](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getEndPaddingMillis())`()` Returns the ending padding duration of this recording in milliseconds since the epoch. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getName())`()` Returns the name of the scheduled recording. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getProgramUri](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getProgramUri())`()` Returns the uri of the scheduled program or series. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRecordingDurationMillis](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getRecordingDurationMillis())`()` The real duration of the recording, including any padding, in milliseconds since the epoch. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getRecordingId](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getRecordingId())`()` Returns the ID of this recording. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRecordingStartTimeMillis](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getRecordingStartTimeMillis())`()` The real start time of the recording, including any padding, in milliseconds since the epoch. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getRecordingUri](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getRecordingUri())`()` The uri of the recording in local storage. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatDays](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getRepeatDays())`()` Returns the days of the week for which this recording should be repeated for. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getScheduledDurationMillis](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getScheduledDurationMillis())`()` Returns the scheduled duration of the recording in milliseconds since the epoch. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getScheduledStartTimeMillis](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getScheduledStartTimeMillis())`()` Returns the scheduled start time of the recording in milliseconds since the epoch. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartPaddingMillis](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getStartPaddingMillis())`()` Returns the start padding duration of this recording in milliseconds since the epoch. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDescription](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#setDescription(kotlin.String))`(`description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets the description of the scheduled recording. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#setName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets the name of the scheduled recording. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TvRecordingInfo](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### FRIDAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRIDAY: Int
```  

 Value: 32

### MONDAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MONDAY: Int
```  

 Value: 2

### RECORDING_ALL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_ALL: Int
```  

 Value: 3

### RECORDING_IN_PROGRESS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_IN_PROGRESS: Int
```  

 Value: 2

### RECORDING_SCHEDULED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RECORDING_SCHEDULED: Int
```  

 Value: 1

### SATURDAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SATURDAY: Int
```  

 Value: 64

### SUNDAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUNDAY: Int
```  

 Value: 1

### THURSDAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val THURSDAY: Int
```  

 Value: 16

### TUESDAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TUESDAY: Int
```  

 Value: 4

### WEDNESDAY

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEDNESDAY: Int
```  

 Value: 8

## Public constructors

### TvRecordingInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TvRecordingInfo(
    recordingId: String, 
    startPadding: Long, 
    endPadding: Long, 
    repeatDays: Int, 
    name: String, 
    description: String, 
    scheduledStartTime: Long, 
    scheduledDuration: Long, 
    channelUri: Uri, 
    programUri: Uri?, 
    contentRatings: MutableList<TvContentRating!>, 
    recordingUri: Uri?, 
    recordingStartTime: Long, 
    recordingDuration: Long)
```

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `recordingId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `channelUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):This value cannot be`null`. |
| `programUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?:This value may be`null`. |
| `contentRatings` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating)!\>:This value cannot be`null`. |
| `recordingUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?:This value may be`null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getChannelUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChannelUri(): Uri
```

Returns the uri of the broadcast channel where the recording will take place.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | This value cannot be`null`. |

### getContentRatings

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentRatings(): MutableList<TvContentRating!>
```

Returns a list of content ratings for the program(s) in this recording.

Returns an empty list if no content rating information is available.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TvContentRating](https://developer.android.com/reference/kotlin/android/media/tv/TvContentRating)!> | This value cannot be`null`. |

### getDescription

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDescription(): String
```

Returns the description of the scheduled recording.

This is set with [TvRecordingInfo.setDescription(String)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#setDescription(kotlin.String))and sent to tv app with [android.media.tv.interactive.TvInteractiveAppService.Session#setTvRecordingInfo(String, TvRecordingInfo)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppService.Session#setTvRecordingInfo(kotlin.String,%20android.media.tv.TvRecordingInfo))

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getEndPaddingMillis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndPaddingMillis(): Long
```

Returns the ending padding duration of this recording in milliseconds since the epoch.

A positive value should cause the recording to end later than the specified time. This should cause the actual duration of the recording to increase. A negative value should cause the recording to end earlier than the specified time. This should cause the actual duration of the recording to decrease. 

### getName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Returns the name of the scheduled recording.

This is set with [TvRecordingInfo.setName(String)](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#setName(kotlin.String))and sent to tv app with [android.media.tv.interactive.TvInteractiveAppService.Session#setTvRecordingInfo(String, TvRecordingInfo)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppService.Session#setTvRecordingInfo(kotlin.String,%20android.media.tv.TvRecordingInfo))

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getProgramUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProgramUri(): Uri?
```

Returns the uri of the scheduled program or series.

For recordings scheduled using scheduleRecording, this value may be null. A non-null programUri implies the started recording should be of that specific program, whereas a null programUri does not impose such a requirement and the recording can span across multiple TV programs. 

### getRecordingDurationMillis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordingDurationMillis(): Long
```

The real duration of the recording, including any padding, in milliseconds since the epoch.

This may not be the same as the value of [getScheduledDurationMillis()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getScheduledDurationMillis())due to a recording starting late, or due to start/end padding.

Returns -1 for recordings that have not yet started.

| Return ||
|------------------------------------------------------------------------------|------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is -1 or greater |

### getRecordingId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordingId(): String
```

Returns the ID of this recording. This ID is created and maintained by the TV app.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getRecordingStartTimeMillis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordingStartTimeMillis(): Long
```

The real start time of the recording, including any padding, in milliseconds since the epoch.

This may not be the same as the value of [getScheduledStartTimeMillis()](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#getScheduledStartTimeMillis())due to a recording starting late, or due to start/end padding.

Returns -1 for recordings that have not yet started.

| Return ||
|------------------------------------------------------------------------------|------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is -1 or greater |

### getRecordingUri

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordingUri(): Uri?
```

The uri of the recording in local storage.

Could be null in the event that the recording has not been completed. 

### getRepeatDays

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRepeatDays(): Int
```

Returns the days of the week for which this recording should be repeated for.

This information is represented in the form of a bitfield, with each bit representing the day which the recording should be repeated.

The bitfield corresponds to each day of the week with the following format:

- [SUNDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#SUNDAY:kotlin.Int)- 0x01 (00000001)
- [MONDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#MONDAY:kotlin.Int)- 0x02 (00000010)
- [TUESDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#TUESDAY:kotlin.Int)- 0x04 (00000100)
- [WEDNESDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#WEDNESDAY:kotlin.Int)- 0x08 (00001000)
- [THURSDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#THURSDAY:kotlin.Int)- 0x10 (00010000)
- [FRIDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#FRIDAY:kotlin.Int)- 0x20 (00100000)
- [SATURDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#SATURDAY:kotlin.Int)- 0x40 (01000000)

You can specify multiple days to repeat the recording by performing a bitwise 'OR' on the bitfield. For example, for a recording to repeat on Sunday and Mondays, this function should return 0x03 (00000011).

A value of 0x00 indicates that the recording will not be repeated.

This format comes from the [Open IPTV Forum Release 2 Specification](https://www.oipf.tv/docs/OIPF-T1-R2_Specification-Volume-5-Declarative-Application-Environment-v2_3-2014-01-24.pdf). It is described in Volume 5, section 7.10.1.1.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.media.tv.TvRecordingInfo#SUNDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#SUNDAY:kotlin.Int), [android.media.tv.TvRecordingInfo#MONDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#MONDAY:kotlin.Int), [android.media.tv.TvRecordingInfo#TUESDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#TUESDAY:kotlin.Int), [android.media.tv.TvRecordingInfo#WEDNESDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#WEDNESDAY:kotlin.Int), [android.media.tv.TvRecordingInfo#THURSDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#THURSDAY:kotlin.Int), [android.media.tv.TvRecordingInfo#FRIDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#FRIDAY:kotlin.Int), and [android.media.tv.TvRecordingInfo#SATURDAY](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#SATURDAY:kotlin.Int) |

### getScheduledDurationMillis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScheduledDurationMillis(): Long
```

Returns the scheduled duration of the recording in milliseconds since the epoch.

| Return ||
|------------------------------------------------------------------------------|-----------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is 0 or greater |

### getScheduledStartTimeMillis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScheduledStartTimeMillis(): Long
```

Returns the scheduled start time of the recording in milliseconds since the epoch.

| Return ||
|------------------------------------------------------------------------------|-----------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is 0 or greater |

### getStartPaddingMillis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartPaddingMillis(): Long
```

Returns the start padding duration of this recording in milliseconds since the epoch.

A positive value should cause the recording to start earlier than the specified time. This should cause the actual duration of the recording to increase. A negative value should cause the recording to start later than the specified time. This should cause the actual duration of the recording to decrease. 

### setDescription

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDescription(description: String): Unit
```

Sets the description of the scheduled recording.

Updates to the [TvRecordingInfo](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#) can be sent to the TV app with [android.media.tv.interactive.TvInteractiveAppService.Session#setTvRecordingInfo(String, TvRecordingInfo)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppService.Session#setTvRecordingInfo(kotlin.String,%20android.media.tv.TvRecordingInfo))

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------|
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

### setName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setName(name: String): Unit
```

Sets the name of the scheduled recording.

Updates to the [TvRecordingInfo](https://developer.android.com/reference/kotlin/android/media/tv/TvRecordingInfo#) can be sent to the TV app with [android.media.tv.interactive.TvInteractiveAppService.Session#setTvRecordingInfo(String, TvRecordingInfo)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppService.Session#setTvRecordingInfo(kotlin.String,%20android.media.tv.TvRecordingInfo))

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TvRecordingInfo!>
```
