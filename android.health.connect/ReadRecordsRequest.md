Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# ReadRecordsRequest

Kotlin | [Java](ReadRecordsRequest.md)
| --- | --- |

```
abstract class ReadRecordsRequest<T : Record!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.ReadRecordsRequest](ReadRecordsRequest.md) |

| Known Direct Subclasses [ReadRecordsRequestUsingFilters](ReadRecordsRequestUsingFilters.md), [ReadRecordsRequestUsingIds](ReadRecordsRequestUsingIds.md) |---|---| | [ReadRecordsRequestUsingFilters](ReadRecordsRequestUsingFilters.md) | Class to represent a request based on time range and data origin filters for readRecords | | [ReadRecordsRequestUsingIds](ReadRecordsRequestUsingIds.md) | A request class to represent request based on RecordIdFilter for readRecords | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A Base class to represent a request for readRecords

## Summary

| Public methods ||
|---|---|
| open [Class](../java.lang/Class.md)\<T\> | getRecordType Returns record type on which read is to be performed |

## Public methods

### getRecordType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getRecordType(): Class<T>
```

Returns record type on which read is to be performed

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>` | This value cannot be `null`. |
