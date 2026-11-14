Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# ReadRecordsRequest

Kotlin | [Java](https://developer.android.com/reference/android/health/connect/ReadRecordsRequest "View this page in Java")

```
abstract class ReadRecordsRequest<T : Record!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.ReadRecordsRequest](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequest#) |

| Known Direct Subclasses [ReadRecordsRequestUsingFilters](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingFilters), [ReadRecordsRequestUsingIds](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds) |---|---| | [ReadRecordsRequestUsingFilters](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingFilters) | Class to represent a request based on time range and data origin filters for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` | | [ReadRecordsRequestUsingIds](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequestUsingIds) | A request class to represent request based on `https://developer.android.com/reference/kotlin/android/health/connect/RecordIdFilter` for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` | |

A Base class to represent a request for `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`

## Summary

| Public methods ||
|---|---|
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\> | `https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsRequest#getRecordType()()` Returns record type on which read is to be performed |

## Public methods

### getRecordType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getRecordType(): Class<T>
```

Returns record type on which read is to be performed

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>` | This value cannot be `null`. |
