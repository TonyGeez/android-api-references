# ChangeLogsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChangeLogsResponse

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/changelog/ChangeLogsResponse "View this page in Java") 

```
class ChangeLogsResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.changelog.ChangeLogsResponse](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#) |

Response class for [HealthConnectManager.getChangeLogs](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#getChangeLogs(android.health.connect.changelog.ChangeLogsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))This is the response to clients fetching changes.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DeletedLog](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse.DeletedLog) A change log holds the [Metadata.getId()](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata.html#getId())of a deleted Record. |
| | [DeletedMedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse.DeletedMedicalResource) A change log holds the [MedicalResourceId](https://developer.android.com/reference/kotlin/android/health/connect/MedicalResourceId.html#) of a deleted medical resource. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ChangeLogsResponse.DeletedLog](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse.DeletedLog)!\> | [getDeletedLogs](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#getDeletedLogs())`()` Returns delete logs for records that have been deleted post the time when the token was retrieved. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ChangeLogsResponse.DeletedMedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse.DeletedMedicalResource)!\> | [getDeletedMedicalResources](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#getDeletedMedicalResources())`()` Returns delete logs for medical resources that have been deleted post the time when the token was retrieved. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getNextChangesToken](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#getNextChangesToken())`()` Returns token for future reads using [HealthConnectManager.getChangeLogs](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#getChangeLogs(android.health.connect.changelog.ChangeLogsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource.html#)!\> | [getUpsertedMedicalResources](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#getUpsertedMedicalResources())`()` Returns medical resources that have been updated or inserted post the time when the given token was generated. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record.html#)!\> | [getUpsertedRecords](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#getUpsertedRecords())`()` Returns records that have been updated or inserted post the time when the given token was generated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMorePages](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#hasMorePages())`()` Returns whether there are more pages available for read. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ChangeLogsResponse](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDeletedLogs

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeletedLogs(): MutableList<ChangeLogsResponse.DeletedLog!>
```

Returns delete logs for records that have been deleted post the time when the token was retrieved.

This contains record ids of deleted records and the timestamps when the records were deleted.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ChangeLogsResponse.DeletedLog](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse.DeletedLog)!> | This value cannot be`null`. |

### getDeletedMedicalResources

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeletedMedicalResources(): MutableList<ChangeLogsResponse.DeletedMedicalResource!>
```

Returns delete logs for medical resources that have been deleted post the time when the token was retrieved.

This contains ids of deleted medical resources and the timestamps when the resources were deleted.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ChangeLogsResponse.DeletedMedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/changelog/ChangeLogsResponse.DeletedMedicalResource)!> | This value cannot be`null`. |

### getNextChangesToken

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNextChangesToken(): String
```

Returns token for future reads using [HealthConnectManager.getChangeLogs](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#getChangeLogs(android.health.connect.changelog.ChangeLogsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getUpsertedMedicalResources

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUpsertedMedicalResources(): MutableList<MedicalResource!>
```

Returns medical resources that have been updated or inserted post the time when the given token was generated.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MedicalResource](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MedicalResource.html#)!> | This value cannot be`null`. |

### getUpsertedRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUpsertedRecords(): MutableList<Record!>
```

Returns records that have been updated or inserted post the time when the given token was generated.

Clients can use the last modified time of the record to check when the record was modified.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record.html#)!> | This value cannot be`null`. |

### hasMorePages

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMorePages(): Boolean
```

Returns whether there are more pages available for read. 

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

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
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ChangeLogsResponse!>
```
