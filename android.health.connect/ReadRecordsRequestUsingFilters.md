Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# ReadRecordsRequestUsingFilters

Kotlin | [Java](ReadRecordsRequestUsingFilters.md)
| --- | --- |

```
class ReadRecordsRequestUsingFilters<T : Record!> : ReadRecordsRequest<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.health.connect.ReadRecordsRequest](ReadRecordsRequest.md)\<T\> ||
| | ↳ | [android.health.connect.ReadRecordsRequestUsingFilters](ReadRecordsRequestUsingFilters.md) |

Class to represent a request based on time range and data origin filters for readRecords

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingFilters.Builder` Builder class for ReadRecordsRequestUsingFilters |

| Public methods ||
|---|---|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [DataOrigin](../android.health.connect.datatypes/DataOrigin.md)!\> | getDataOrigins Returns the set of DataOrigin to be read, or empty list for no filter |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPageSize Returns maximum number of records to be returned by the read operation |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getPageToken Returns page token to read the current page of the result. |
| --- | --- |
| [TimeRangeFilter](TimeRangeFilter.md)? | getTimeRangeFilter Returns time range b/w which the read operation is to be performed |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAscending Returns ordering of results to be returned |

| Inherited functions ||
|---|---|
| From class ReadRecordsRequest |---|---| | `https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>` | getRecordType Returns record type on which read is to be performed <br /> | ||

## Public methods

### getDataOrigins

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getDataOrigins(): MutableSet<DataOrigin!>
```

Returns the set of DataOrigin to be read, or empty list for no filter

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin!>` | This value cannot be `null`. |

### getPageSize

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPageSize(): Int
```

Returns maximum number of records to be returned by the read operation

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is between 1 and 5000 inclusive |

### getPageToken

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPageToken(): Long
```

Returns page token to read the current page of the result. -1 if none available

### getTimeRangeFilter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTimeRangeFilter(): TimeRangeFilter?
```

Returns time range b/w which the read operation is to be performed

| Return ||
|---|---|
| TimeRangeFilter | This value may be `null`. |

### isAscending

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun isAscending(): Boolean
```

Returns ordering of results to be returned
