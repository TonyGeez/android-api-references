# ReadRecordsRequestUsingIds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadRecordsRequestUsingIds

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/ReadRecordsRequestUsingIds "View this page in Java") 
| --- | --- |

```
class ReadRecordsRequestUsingIds<T : Record!> : ReadRecordsRequest<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.health.connect.ReadRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequest)\<T\> ||
| | ↳ | [android.health.connect.ReadRecordsRequestUsingIds](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds#) |

A request class to represent request based on [RecordIdFilters](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter) for [android.health.connect.HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,java.util.concurrent.Executor,android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))

A [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter) can be constructed with either [record ID](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#fromId(java.lang.Class,%20kotlin.String))or [client record ID](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter#fromClientRecordId(java.lang.Class,%20kotlin.String)). However, it's worth noting that only reading with own client record IDs is allowed, using client record IDs to read records inserted by another app will return no result.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds.Builder) Builder class for [ReadRecordsRequestUsingIds](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds#) |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter)!\> | [getRecordIdFilters](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds#getRecordIdFilters())`()` Returns List of RecordId |

| Inherited functions ||
|---|---|
| From class [ReadRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequest) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T> | [getRecordType](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequest#getRecordType())`()` <br /> Returns record type on which read is to be performed <br /> | ||

## Public methods

### getRecordIdFilters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordIdFilters(): MutableList<RecordIdFilter!>
```

Returns List of RecordId

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RecordIdFilter](https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter)!> | This value cannot be`null`. |
