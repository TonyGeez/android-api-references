# ReadRecordsRequestUsingIds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadRecordsRequestUsingIds

Kotlin| [Java](ReadRecordsRequestUsingIds.md) 
| --- | --- |

```
class ReadRecordsRequestUsingIds<T : Record!> : ReadRecordsRequest<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.health.connect.ReadRecordsRequest](ReadRecordsRequest.md)\<T\> ||
| | ↳ | [android.health.connect.ReadRecordsRequestUsingIds](ReadRecordsRequestUsingIds.md) |

A request class to represent request based on [RecordIdFilters](RecordIdFilter.md) for [android.health.connect.HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,java.util.concurrent.Executor,android.os.OutcomeReceiver)](HealthConnectManager.md))

A [RecordIdFilter](RecordIdFilter.md) can be constructed with either [record ID](RecordIdFilter.md))or [client record ID](RecordIdFilter.md)). However, it's worth noting that only reading with own client record IDs is allowed, using client record IDs to read records inserted by another app will return no result.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/ReadRecordsRequestUsingIds.Builder.md) Builder class for [ReadRecordsRequestUsingIds](ReadRecordsRequestUsingIds.md) |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RecordIdFilter](RecordIdFilter.md)!\> | [getRecordIdFilters](ReadRecordsRequestUsingIds.md))`()` Returns List of RecordId |

| Inherited functions ||
|---|---|
| From class [ReadRecordsRequest](ReadRecordsRequest.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Class](../java.lang/Class.md)<T> | [getRecordType](ReadRecordsRequest.md))`()` <br /> Returns record type on which read is to be performed <br /> | ||

## Public methods

### getRecordIdFilters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordIdFilters(): MutableList<RecordIdFilter!>
```

Returns List of RecordId

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RecordIdFilter](RecordIdFilter.md)!> | This value cannot be`null`. |
