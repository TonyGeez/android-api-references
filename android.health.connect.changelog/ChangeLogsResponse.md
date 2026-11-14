# ChangeLogsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChangeLogsResponse

Kotlin| [Java](../android/health/connect/changelog/ChangeLogsResponse.md) 
| --- | --- |

```
class ChangeLogsResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.changelog.ChangeLogsResponse](../android/health/connect/changelog/ChangeLogsResponse.md) |

Response class for [HealthConnectManager.getChangeLogs](../android/health/connect/HealthConnectManager.md))This is the response to clients fetching changes.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DeletedLog](../android/health/connect/changelog/ChangeLogsResponse.DeletedLog.md) A change log holds the [Metadata.getId()](../android/health/connect/datatypes/Metadata.md))of a deleted Record. |
| | [DeletedMedicalResource](../android/health/connect/changelog/ChangeLogsResponse.DeletedMedicalResource.md) A change log holds the [MedicalResourceId](../android/health/connect/MedicalResourceId.md) of a deleted medical resource. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/health/connect/changelog/ChangeLogsResponse.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/health/connect/changelog/ChangeLogsResponse.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ChangeLogsResponse.DeletedLog](../android/health/connect/changelog/ChangeLogsResponse.DeletedLog.md)!\> | [getDeletedLogs](../android/health/connect/changelog/ChangeLogsResponse.md))`()` Returns delete logs for records that have been deleted post the time when the token was retrieved. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ChangeLogsResponse.DeletedMedicalResource](../android/health/connect/changelog/ChangeLogsResponse.DeletedMedicalResource.md)!\> | [getDeletedMedicalResources](../android/health/connect/changelog/ChangeLogsResponse.md))`()` Returns delete logs for medical resources that have been deleted post the time when the token was retrieved. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getNextChangesToken](../android/health/connect/changelog/ChangeLogsResponse.md))`()` Returns token for future reads using [HealthConnectManager.getChangeLogs](../android/health/connect/HealthConnectManager.md)). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MedicalResource](../android/health/connect/datatypes/MedicalResource.md)!\> | [getUpsertedMedicalResources](../android/health/connect/changelog/ChangeLogsResponse.md))`()` Returns medical resources that have been updated or inserted post the time when the given token was generated. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Record](../android/health/connect/datatypes/Record.md)!\> | [getUpsertedRecords](../android/health/connect/changelog/ChangeLogsResponse.md))`()` Returns records that have been updated or inserted post the time when the given token was generated. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMorePages](../android/health/connect/changelog/ChangeLogsResponse.md))`()` Returns whether there are more pages available for read. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/health/connect/changelog/ChangeLogsResponse.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/health/connect/changelog/ChangeLogsResponse.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ChangeLogsResponse](../android/health/connect/changelog/ChangeLogsResponse.md)!\> | [CREATOR](../android/health/connect/changelog/ChangeLogsResponse.md) <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ChangeLogsResponse.DeletedLog](../android/health/connect/changelog/ChangeLogsResponse.DeletedLog.md)!> | This value cannot be`null`. |

### getDeletedMedicalResources

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeletedMedicalResources(): MutableList<ChangeLogsResponse.DeletedMedicalResource!>
```

Returns delete logs for medical resources that have been deleted post the time when the token was retrieved.

This contains ids of deleted medical resources and the timestamps when the resources were deleted.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ChangeLogsResponse.DeletedMedicalResource](../android/health/connect/changelog/ChangeLogsResponse.DeletedMedicalResource.md)!> | This value cannot be`null`. |

### getNextChangesToken

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNextChangesToken(): String
```

Returns token for future reads using [HealthConnectManager.getChangeLogs](../android/health/connect/HealthConnectManager.md)).

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MedicalResource](../android/health/connect/datatypes/MedicalResource.md)!> | This value cannot be`null`. |

### getUpsertedRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUpsertedRecords(): MutableList<Record!>
```

Returns records that have been updated or inserted post the time when the given token was generated.

Clients can use the last modified time of the record to check when the record was modified.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Record](../android/health/connect/datatypes/Record.md)!> | This value cannot be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ChangeLogsResponse!>
```
