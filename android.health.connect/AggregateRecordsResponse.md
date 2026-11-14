# AggregateRecordsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AggregateRecordsResponse

Kotlin| [Java](../android/health/connect/AggregateRecordsResponse.md) 
| --- | --- |

```
class AggregateRecordsResponse<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.AggregateRecordsResponse](../android/health/connect/AggregateRecordsResponse.md) |

A class representing response for [HealthConnectManager.aggregate](../android/health/connect/HealthConnectManager.md))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T? | [get](../android/health/connect/AggregateRecordsResponse.md))`(`aggregationType:` ` [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>`)` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [DataOrigin](../android/health/connect/datatypes/DataOrigin.md)!\> | [getDataOrigins](../android/health/connect/AggregateRecordsResponse.md))`(`aggregationType:` ` [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>`)` Returns a set of [DataOrigin](../android/health/connect/datatypes/DataOrigin.md) s for the underlying aggregation record, empty set if the corresponding aggregation doesn't exist and or if multiple records were present. |
| [ZoneOffset](../java/time/ZoneOffset.md)? | [getZoneOffset](../android/health/connect/AggregateRecordsResponse.md))`(`aggregationType:` ` [AggregationType](../android/health/connect/datatypes/AggregationType.md)<T>`)` <br /> |
| --- | --- |

## Public methods

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(aggregationType: AggregationType<T>): T?
```

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](../android/health/connect/datatypes/AggregationType.md)\<T\>: [AggregationType](../android/health/connect/datatypes/AggregationType.md) for which to get the result This value cannot be`null`. |

| Return ||
|----|-------------------------------------------------------------------------|
| T? | an aggregation result for`aggregationType`. \* This value may be`null`. |

### getDataOrigins

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getZoneOffset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZoneOffset(aggregationType: AggregationType<T>): ZoneOffset?
```

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](../android/health/connect/datatypes/AggregationType.md)\<T\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ZoneOffset](../java/time/ZoneOffset.md)? | [ZoneOffset](../java/time/ZoneOffset.md) for the underlying aggregation record, null if the corresponding aggregation doesn't exist and or if multiple records were present. |
