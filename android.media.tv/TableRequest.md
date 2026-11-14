# TableRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TableRequest

Kotlin| [Java](TableRequest.md) 
| --- | --- |

```
class TableRequest : BroadcastInfoRequest, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.tv.BroadcastInfoRequest](BroadcastInfoRequest.md) ||
| | ↳ | [android.media.tv.TableRequest](TableRequest.md) |

A request for Table from broadcast signal.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_BAT](TableRequest.md) Bouquet Association Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_CAT](TableRequest.md) Conditional Access Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_EIT](TableRequest.md) Event Information Table |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_NIT](TableRequest.md) Network Information Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_PAT](TableRequest.md) Program Association Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_PMT](TableRequest.md) Program Mapping Table |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_SDT](TableRequest.md) Service Description Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_SIT](TableRequest.md) Selection Information Table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_TDT](TableRequest.md) Time and Date Table |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TABLE_NAME_TOT](TableRequest.md) Time Offset Table |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [BroadcastInfoRequest](BroadcastInfoRequest.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_AUTO_UPDATE](BroadcastInfoRequest.md) <br /> Request option: auto update. With this option, a response is sent only when broadcast information is detected for the first time, new values are detected. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONESHOT](BroadcastInfoRequest.md) <br /> Request option: one-shot With this option, only one response will be given per request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONEWAY](BroadcastInfoRequest.md) <br /> Request option: one-way With this option, no response is expected after sending the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_REPEAT](BroadcastInfoRequest.md) <br /> Request option: repeat. With this option, a response is sent when related broadcast information is detected, even if the same information has been sent previously. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TableRequest](TableRequest.md))`(`requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tableId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tableName:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](TableRequest.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTableId](TableRequest.md))`()` Gets the ID of requested table. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTableName](TableRequest.md))`()` Gets the name of requested table. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](TableRequest.md))`()` Gets the version number of requested table. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](TableRequest.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [BroadcastInfoRequest](BroadcastInfoRequest.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOption](BroadcastInfoRequest.md))`()` <br /> Gets the request option of the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](BroadcastInfoRequest.md))`()` <br /> Gets the ID of the request. The ID is used to associate the response with the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](BroadcastInfoRequest.md))`()` <br /> Gets the broadcast info type. The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TableRequest](TableRequest.md)!\> | [CREATOR](TableRequest.md) <br /> |

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
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_REPEAT](BroadcastInfoRequest.md), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE](BroadcastInfoRequest.md), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONEWAY](BroadcastInfoRequest.md), or [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONESHOT](BroadcastInfoRequest.md) |
| `tableName` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.TableRequest#TABLE_NAME_PAT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_PMT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_CAT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_NIT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_BAT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_SDT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_EIT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_TDT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_TOT](TableRequest.md), or [android.media.tv.TableRequest#TABLE_NAME_SIT](TableRequest.md) |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.TableRequest#TABLE_NAME_PAT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_PMT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_CAT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_NIT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_BAT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_SDT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_EIT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_TDT](TableRequest.md), [android.media.tv.TableRequest#TABLE_NAME_TOT](TableRequest.md), or [android.media.tv.TableRequest#TABLE_NAME_SIT](TableRequest.md) |

### getVersion

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): Int
```

Gets the version number of requested table. If it is null, value will be -1.

The consistency of version numbers between request and response depends on [BroadcastInfoRequest.getOption()](BroadcastInfoRequest.md)). If the request has RequestOption value REQUEST_OPTION_AUTO_UPDATE, then the response may be set to the latest version which may be different from the version of the request. Otherwise, response with a different version from its request will be considered invalid. 

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TableRequest!>
```
