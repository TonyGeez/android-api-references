# AggregateRecordsRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AggregateRecordsRequest

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/AggregateRecordsRequest "View this page in Java") 
| --- | --- |

```
class AggregateRecordsRequest<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.AggregateRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest#) |

A class to create requests for [HealthConnectManager.aggregate](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregate(android.health.connect.AggregateRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest.Builder) <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\<T\>!\> | [getAggregationTypes](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest#getAggregationTypes())`()` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [DataOrigin](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin)!\> | [getDataOriginsFilters](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest#getDataOriginsFilters())`()` <br /> |
| [TimeRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeRangeFilter) | [getTimeRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsRequest#getTimeRangeFilter())`()` <br /> |
| --- | --- |

## Public methods

### getAggregationTypes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAggregationTypes(): MutableSet<AggregationType<T>!>
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)<T>!> | Set of integers from [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType) to aggregate This value cannot be`null`. |

### getDataOriginsFilters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataOriginsFilters(): MutableSet<DataOrigin!>
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [DataOrigin](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin)!> | Set of [DataOrigin](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin) s to read from, or empty set for no filter This value cannot be`null`. |

### getTimeRangeFilter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeRangeFilter(): TimeRangeFilter
```

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [TimeRangeFilter](https://developer.android.com/reference/kotlin/android/health/connect/TimeRangeFilter) | time range b/w which the aggregate operation is to be performed This value cannot be`null`. |
