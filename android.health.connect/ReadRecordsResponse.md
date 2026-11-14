# ReadRecordsResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadRecordsResponse

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/ReadRecordsResponse "View this page in Java") 
| --- | --- |

```
open class ReadRecordsResponse<T : Record!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.ReadRecordsResponse](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsResponse#) |

Response containing list of Records for [HealthConnectManager.readRecords](https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager#readRecords(android.health.connect.ReadRecordsRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNextPageToken](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsResponse#getNextPageToken())`()` Returns a page token to read the next page of the result. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | [getRecords](https://developer.android.com/reference/kotlin/android/health/connect/ReadRecordsResponse#getRecords())`()` <br /> |

## Public methods

### getNextPageToken

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNextPageToken(): Long
```

Returns a page token to read the next page of the result. -1 if there are no more pages available. 

### getRecords

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRecords(): MutableList<T>
```

| Return ||
|------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T> | This value cannot be`null`. |
