# AggregateRecordsRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AggregateRecordsRequest

Kotlin| [Java](../android/health/connect/AggregateRecordsRequest.md) 
| --- | --- |

```
class AggregateRecordsRequest<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.AggregateRecordsRequest](../android/health/connect/AggregateRecordsRequest.md) |

A class to create requests for [HealthConnectManager.aggregate](../android/health/connect/HealthConnectManager.md))

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/AggregateRecordsRequest.Builder.md) <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AggregationType](../android/health/connect/datatypes/AggregationType.md)\<T\>!\> | [getAggregationTypes](../android/health/connect/AggregateRecordsRequest.md))`()` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [DataOrigin](../android/health/connect/datatypes/DataOrigin.md)!\> | [getDataOriginsFilters](../android/health/connect/AggregateRecordsRequest.md))`()` <br /> |
| [TimeRangeFilter](../android/health/connect/TimeRangeFilter.md) | [getTimeRangeFilter](../android/health/connect/AggregateRecordsRequest.md))`()` <br /> |
| --- | --- |

## Public methods

### getAggregationTypes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAggregationTypes(): MutableSet<AggregationType<T>!>
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>!> | Set of integers from [AggregationType](../android/health/connect/datatypes/AggregationType.md) to aggregate This value cannot be`null`. |

### getDataOriginsFilters

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataOriginsFilters(): MutableSet<DataOrigin!>
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [DataOrigin](../android/health/connect/datatypes/DataOrigin.md)!> | Set of [DataOrigin](../android/health/connect/datatypes/DataOrigin.md) s to read from, or empty set for no filter This value cannot be`null`. |

### getTimeRangeFilter

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeRangeFilter(): TimeRangeFilter
```

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [TimeRangeFilter](../android/health/connect/TimeRangeFilter.md) | time range b/w which the aggregate operation is to be performed This value cannot be`null`. |
