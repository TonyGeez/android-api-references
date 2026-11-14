# InsertRecordsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InsertRecordsResponse

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/InsertRecordsResponse "View this page in Java") 
| --- | --- |

```
open class InsertRecordsResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.InsertRecordsResponse](https://developer.android.com/reference/kotlin/android/health/connect/InsertRecordsResponse#) |

Response for [HealthConnectManager.insertRecords](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#insertRecords(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)). The response contains records in same order as records in [HealthConnectManager.insertRecords](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#insertRecords(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!\> | [getRecords](https://developer.android.com/reference/kotlin/android/health/connect/InsertRecordsResponse#getRecords())`()` <br /> |

## Public methods

### getRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecords(): MutableList<Record!>
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record)!> | This value cannot be`null`. |
