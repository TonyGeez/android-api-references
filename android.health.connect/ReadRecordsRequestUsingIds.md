# ReadRecordsRequestUsingIds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadRecordsRequestUsingIds

Kotlin| [Java](../android/health/connect/ReadRecordsRequestUsingIds.md) 
| --- | --- |

```
class ReadRecordsRequestUsingIds<T : Record!> : ReadRecordsRequest<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.health.connect.ReadRecordsRequest](../android/health/connect/ReadRecordsRequest.md)\<T\> ||
| | ↳ | [android.health.connect.ReadRecordsRequestUsingIds](../android/health/connect/ReadRecordsRequestUsingIds.md) |

A request class to represent request based on [RecordIdFilters](../android/health/connect/RecordIdFilter.md) for [android.health.connect.HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,java.util.concurrent.Executor,android.os.OutcomeReceiver)](../android/health/connect/HealthConnectManager.md))

A [RecordIdFilter](../android/health/connect/RecordIdFilter.md) can be constructed with either [record ID](../android/health/connect/RecordIdFilter.md))or [client record ID](../android/health/connect/RecordIdFilter.md)). However, it's worth noting that only reading with own client record IDs is allowed, using client record IDs to read records inserted by another app will return no result.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/ReadRecordsRequestUsingIds.Builder.md) Builder class for [ReadRecordsRequestUsingIds](../android/health/connect/ReadRecordsRequestUsingIds.md) |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RecordIdFilter](../android/health/connect/RecordIdFilter.md)!\> | [getRecordIdFilters](../android/health/connect/ReadRecordsRequestUsingIds.md))`()` Returns List of RecordId |

| Inherited functions ||
|---|---|
| From class [ReadRecordsRequest](../android/health/connect/ReadRecordsRequest.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Class](../java/lang/Class.md)<T> | [getRecordType](../android/health/connect/ReadRecordsRequest.md))`()` <br /> Returns record type on which read is to be performed <br /> | ||

## Public methods

### getRecordIdFilters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordIdFilters(): MutableList<RecordIdFilter!>
```

Returns List of RecordId

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RecordIdFilter](../android/health/connect/RecordIdFilter.md)!> | This value cannot be`null`. |
