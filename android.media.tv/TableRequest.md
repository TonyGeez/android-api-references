# TableRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TableRequest

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/TableRequest "View this page in Java") 
| --- | --- |

```
class TableRequest : BroadcastInfoRequest, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.tv.BroadcastInfoRequest](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest) ||
| | ↳ | [android.media.tv.TableRequest](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#) |

A request for Table from broadcast signal.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_BAT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_BAT:kotlin.Int) Bouquet Association Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_CAT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_CAT:kotlin.Int) Conditional Access Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_EIT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_EIT:kotlin.Int) Event Information Table |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_NIT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_NIT:kotlin.Int) Network Information Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_PAT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_PAT:kotlin.Int) Program Association Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_PMT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_PMT:kotlin.Int) Program Mapping Table |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_SDT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_SDT:kotlin.Int) Service Description Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_SIT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_SIT:kotlin.Int) Selection Information Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_TDT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_TDT:kotlin.Int) Time and Date Table |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_TOT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_TOT:kotlin.Int) Time Offset Table |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [BroadcastInfoRequest](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_AUTO_UPDATE](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE:kotlin.Int) <br /> Request option: auto update. With this option, a response is sent only when broadcast information is detected for the first time, new values are detected. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONESHOT](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONESHOT:kotlin.Int) <br /> Request option: one-shot With this option, only one response will be given per request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONEWAY](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONEWAY:kotlin.Int) <br /> Request option: one-way With this option, no response is expected after sending the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_REPEAT](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_REPEAT:kotlin.Int) <br /> Request option: repeat. With this option, a response is sent when related broadcast information is detected, even if the same information has been sent previously. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TableRequest](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TableRequest(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tableId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tableName:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTableId](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#getTableId())`()` Gets the ID of requested table. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTableName](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#getTableName())`()` Gets the name of requested table. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#getVersion())`()` Gets the version number of requested table. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [BroadcastInfoRequest](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOption](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getOption())`()` <br /> Gets the request option of the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getRequestId())`()` <br /> Gets the ID of the request. The ID is used to associate the response with the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getType())`()` <br /> Gets the broadcast info type. The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TableRequest](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### TABLE_NAME_BAT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_BAT: Int
```

Bouquet Association Table 

 Value: 4

### TABLE_NAME_CAT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_CAT: Int
```

Conditional Access Table 

 Value: 2

### TABLE_NAME_EIT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_EIT: Int
```

Event Information Table 

 Value: 6

### TABLE_NAME_NIT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_NIT: Int
```

Network Information Table 

 Value: 3

### TABLE_NAME_PAT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_PAT: Int
```

Program Association Table 

 Value: 0

### TABLE_NAME_PMT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_PMT: Int
```

Program Mapping Table 

 Value: 1

### TABLE_NAME_SDT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_SDT: Int
```

Service Description Table 

 Value: 5

### TABLE_NAME_SIT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_SIT: Int
```

Selection Information Table 

 Value: 9

### TABLE_NAME_TDT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_TDT: Int
```

Time and Date Table 

 Value: 7

### TABLE_NAME_TOT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TABLE_NAME_TOT: Int
```

Time Offset Table 

 Value: 8

## Public constructors

### TableRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TableRequest(
    requestId: Int, 
    option: Int, 
    tableId: Int, 
    tableName: Int, 
    version: Int)
```

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_REPEAT](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_REPEAT:kotlin.Int), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE:kotlin.Int), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONEWAY](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONEWAY:kotlin.Int), or [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONESHOT](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONESHOT:kotlin.Int) |
| `tableName` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.TableRequest#TABLE_NAME_PAT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_PAT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_PMT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_PMT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_CAT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_CAT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_NIT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_NIT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_BAT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_BAT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_SDT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_SDT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_EIT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_EIT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_TDT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_TDT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_TOT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_TOT:kotlin.Int), or [android.media.tv.TableRequest#TABLE_NAME_SIT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_SIT:kotlin.Int) |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getTableId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTableId(): Int
```

Gets the ID of requested table. 

### getTableName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTableName(): Int
```

Gets the name of requested table.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.TableRequest#TABLE_NAME_PAT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_PAT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_PMT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_PMT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_CAT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_CAT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_NIT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_NIT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_BAT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_BAT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_SDT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_SDT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_EIT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_EIT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_TDT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_TDT:kotlin.Int), [android.media.tv.TableRequest#TABLE_NAME_TOT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_TOT:kotlin.Int), or [android.media.tv.TableRequest#TABLE_NAME_SIT](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest#TABLE_NAME_SIT:kotlin.Int) |

### getVersion

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): Int
```

Gets the version number of requested table. If it is null, value will be -1.

The consistency of version numbers between request and response depends on [BroadcastInfoRequest.getOption()](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getOption()). If the request has RequestOption value REQUEST_OPTION_AUTO_UPDATE, then the response may be set to the latest version which may be different from the version of the request. Otherwise, response with a different version from its request will be considered invalid. 

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
static val CREATOR: Parcelable.Creator<TableRequest!>
```
