# AggregateRecordsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AggregateRecordsResponse

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/AggregateRecordsResponse "View this page in Java") 

```
class AggregateRecordsResponse<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.AggregateRecordsResponse](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsResponse#) |

A class representing response for [HealthConnectManager.aggregate](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregate(android.health.connect.AggregateRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T? | [get](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsResponse#get(android.health.connect.datatypes.AggregationType))`(`aggregationType:` ` [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)<T>`)` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [DataOrigin](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin)!\> | [getDataOrigins](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsResponse#getDataOrigins(android.health.connect.datatypes.AggregationType))`(`aggregationType:` ` [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)<T>`)` Returns a set of [DataOrigin](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin) s for the underlying aggregation record, empty set if the corresponding aggregation doesn't exist and or if multiple records were present. |
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)? | [getZoneOffset](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsResponse#getZoneOffset(android.health.connect.datatypes.AggregationType))`(`aggregationType:` ` [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)<T>`)` <br /> |

## Public methods

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(aggregationType: AggregationType<T>): T?
```

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\<T\>: [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType) for which to get the result This value cannot be`null`. |

| Return ||
|----|-------------------------------------------------------------------------|
| T? | an aggregation result for`aggregationType`. \* This value may be`null`. |

### getDataOrigins

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataOrigins(aggregationType: AggregationType<T>): MutableSet<DataOrigin!>
```

Returns a set of [DataOrigin](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin) s for the underlying aggregation record, empty set if the corresponding aggregation doesn't exist and or if multiple records were present.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\<T\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [DataOrigin](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin)!> | This value cannot be`null`. |

### getZoneOffset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZoneOffset(aggregationType: AggregationType<T>): ZoneOffset?
```

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\<T\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)? | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#) for the underlying aggregation record, null if the corresponding aggregation doesn't exist and or if multiple records were present. |
