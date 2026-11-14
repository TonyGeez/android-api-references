# AggregateRecordsGroupedByDurationResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AggregateRecordsGroupedByDurationResponse

Kotlin| [Java](../android/health/connect/AggregateRecordsGroupedByDurationResponse.md) 
| --- | --- |

```
class AggregateRecordsGroupedByDurationResponse<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.AggregateRecordsGroupedByDurationResponse](../android/health/connect/AggregateRecordsGroupedByDurationResponse.md) |

Class to represent the response from [HealthConnectManager.aggregateGroupByDuration](../android/health/connect/HealthConnectManager.md))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T? | [get](../android/health/connect/AggregateRecordsGroupedByDurationResponse.md))`(`aggregationType:` ` [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>`)` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [DataOrigin](../android/health/connect/datatypes/DataOrigin.md)!\> | [getDataOrigins](../android/health/connect/AggregateRecordsGroupedByDurationResponse.md))`(`aggregationType:` ` [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>`)` Returns a set of [DataOrigin](../android/health/connect/datatypes/DataOrigin.md) s for the underlying aggregation record, empty set if the corresponding aggregation doesn't exist and or if multiple records were present. |
| [Instant](../java/time/Instant.md) | [getEndTime](../android/health/connect/AggregateRecordsGroupedByDurationResponse.md))`()` <br /> |
| --- | --- |
| [Instant](../java/time/Instant.md) | [getStartTime](../android/health/connect/AggregateRecordsGroupedByDurationResponse.md))`()` <br /> |
| [ZoneOffset](../java/time/ZoneOffset.md)? | [getZoneOffset](../android/health/connect/AggregateRecordsGroupedByDurationResponse.md))`(`aggregationType:` ` [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>`)` <br /> |

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
fun getEndTime(): Instant
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Instant](../java/time/Instant.md) | End time of the window for the underlying aggregation This value cannot be`null`. |

### getStartTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTime(): Instant
```

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Instant](../java/time/Instant.md) | Start time of the window for the underlying aggregation This value cannot be`null`. |

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
