# AggregateRecordsGroupedByPeriodResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AggregateRecordsGroupedByPeriodResponse

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/AggregateRecordsGroupedByPeriodResponse "View this page in Java") 

```
class AggregateRecordsGroupedByPeriodResponse<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.AggregateRecordsGroupedByPeriodResponse](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse#) |

Class to represent the response from [HealthConnectManager.aggregateGroupByPeriod](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#aggregateGroupByPeriod(android.health.connect.AggregateRecordsRequest,%20java.time.Period,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T? | [get](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse#get(android.health.connect.datatypes.AggregationType))`(`aggregationType:` ` [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)<T>`)` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [DataOrigin](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin)!\> | [getDataOrigins](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse#getDataOrigins(android.health.connect.datatypes.AggregationType))`(`aggregationType:` ` [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)<T>`)` Returns a set of [DataOrigin](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DataOrigin) s for the underlying aggregation record, empty set if the corresponding aggregation doesn't exist and or if multiple records were present. |
| [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) | [getEndTime](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse#getEndTime())`()` <br /> |
| [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) | [getStartTime](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse#getStartTime())`()` <br /> |
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)? | [getZoneOffset](https://developer.android.com/reference/kotlin/android/health/connect/AggregateRecordsGroupedByPeriodResponse#getZoneOffset(android.health.connect.datatypes.AggregationType))`(`aggregationType:` ` [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)<T>`)` <br /> |

## Public methods

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(aggregationType: AggregationType<T>): T?
```

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\<T\>:This value cannot be`null`. |

| Return ||
|----|---------------------------------------------------------------------------|
| T? | An aggregation result for`aggregationType`, and null if one doesn't exist |

### getDataOrigins

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions) 

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

### getEndTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndTime(): LocalDateTime
```

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) | End [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) of the window for the underlying aggregation This value cannot be`null`. |

### getStartTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTime(): LocalDateTime
```

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) | Start [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#) of the window for the underlying aggregation This value cannot be`null`. |

### getZoneOffset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZoneOffset(aggregationType: AggregationType<T>): ZoneOffset?
```

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `aggregationType` | [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\<T\>:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)? | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#) for the underlying aggregation record, null if the corresponding aggregation doesn't exist or if multiple records were present. |
