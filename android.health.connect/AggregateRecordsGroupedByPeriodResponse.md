# AggregateRecordsGroupedByPeriodResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AggregateRecordsGroupedByPeriodResponse

Kotlin| [Java](../android/health/connect/AggregateRecordsGroupedByPeriodResponse.md) 
| --- | --- |

```
class AggregateRecordsGroupedByPeriodResponse<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.AggregateRecordsGroupedByPeriodResponse](../android/health/connect/AggregateRecordsGroupedByPeriodResponse.md) |

Class to represent the response from [HealthConnectManager.aggregateGroupByPeriod](../android/health/connect/HealthConnectManager.md))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T? | [get](../android/health/connect/AggregateRecordsGroupedByPeriodResponse.md))`(`aggregationType:` ` [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>`)` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [DataOrigin](../android/health/connect/datatypes/DataOrigin.md)!\> | [getDataOrigins](../android/health/connect/AggregateRecordsGroupedByPeriodResponse.md))`(`aggregationType:` ` [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>`)` Returns a set of [DataOrigin](../android/health/connect/datatypes/DataOrigin.md) s for the underlying aggregation record, empty set if the corresponding aggregation doesn't exist and or if multiple records were present. |
| [LocalDateTime](../java/time/LocalDateTime.md) | [getEndTime](../android/health/connect/AggregateRecordsGroupedByPeriodResponse.md))`()` <br /> |
| --- | --- |
| [LocalDateTime](../java/time/LocalDateTime.md) | [getStartTime](../android/health/connect/AggregateRecordsGroupedByPeriodResponse.md))`()` <br /> |
| [ZoneOffset](../java/time/ZoneOffset.md)? | [getZoneOffset](../android/health/connect/AggregateRecordsGroupedByPeriodResponse.md))`(`aggregationType:` ` [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>`)` <br /> |

## Public methods

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(aggregationType: AggregationType<T>): T?
```

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](../android/health/connect/datatypes/AggregationType.md)\<T\>:This value cannot be`null`. |

| Return ||
|----|---------------------------------------------------------------------------|
| T? | An aggregation result for`aggregationType`, and null if one doesn't exist |

### getDataOrigins

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions) 

```
fun getDataOrigins(aggregationType: AggregationType<T>): MutableSet<DataOrigin!>
```

Returns a set of [DataOrigin](../android/health/connect/datatypes/DataOrigin.md) s for the underlying aggregation record, empty set if the corresponding aggregation doesn't exist and or if multiple records were present.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](../android/health/connect/datatypes/AggregationType.md)\<T\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [DataOrigin](../android/health/connect/datatypes/DataOrigin.md)!> | This value cannot be`null`. |

### getEndTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndTime(): LocalDateTime
```

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalDateTime](../java/time/LocalDateTime.md) | End [LocalDateTime](../java/time/LocalDateTime.md) of the window for the underlying aggregation This value cannot be`null`. |

### getStartTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTime(): LocalDateTime
```

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalDateTime](../java/time/LocalDateTime.md) | Start [LocalDateTime](../java/time/LocalDateTime.md) of the window for the underlying aggregation This value cannot be`null`. |

### getZoneOffset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZoneOffset(aggregationType: AggregationType<T>): ZoneOffset?
```

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](../android/health/connect/datatypes/AggregationType.md)\<T\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ZoneOffset](../java/time/ZoneOffset.md)? | [ZoneOffset](../java/time/ZoneOffset.md) for the underlying aggregation record, null if the corresponding aggregation doesn't exist or if multiple records were present. |
